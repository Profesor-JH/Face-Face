# Nice-Face

Welcome to the Nice-Face project. This application leverages advanced machine learning and natural language processing techniques to assist investors in analyzing market sentiments and detecting relevant topics from a vast amount of unstructured data. By utilizing OpenAI's GPT-3.5 and Weaviate, Nice-Face provides detailed, relevant, and professionally formatted responses based on the user's queries and contextual data retrieved from various sources.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Real-time market sentiment analysis**: Get detailed insights and analysis based on real-time data.
- **Contextual responses**: Integrates with Weaviate to fetch relevant context for better response accuracy.
- **Streaming responses**: Provides partial responses in real-time to ensure faster user interaction.
- **Easy integration**: Built with FastAPI and Socket.IO for easy integration and real-time capabilities.

## Installation
### Prerequisites
- Python 3.8 or higher
- Docker (for Weaviate setup)
- MySQL server (for storing stock news data)

### Clone the Repository
```bash
git clone https://github.com/Profesor-JH/Nice-Face.git
cd Nice-Face
```

### Install Dependencies
It is recommended to use a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
pip install -r requirements.txt
```

### Environment Variables
Create a `.env` file in the project root directory and add your OpenAI API key:

```OPENAI_API_KEY=your_openai_api_key_here
```

## Usage

To start the application, run:

``` bash 
uvicorn main:app --host 0.0.0.0 --port 6789 --reload
```
The application will be available at `http://localhost:6789`.

## Configuration

The application uses a `config.yaml` file for MySQL database configuration. An example configuration is shown below:

```
database:
  host: localhost
  user: your_username
  password: your_password
  database: your_database
```

## File Structure

```
Nice-Face/
│
├── main.py                # Main application file
├── backendtest.py         # Backend test file
├── config.yaml            # Configuration file
├── README.md              # Project documentation
├── requirements.txt       # Python dependencies
├── weaviate/              # Directory for Weaviate interface and related files
│   ├── __init__.py
│   └── weaviate_interface.py
└── hidding_app/           # Directory for additional modules and helpers
    ├── __init__.py
    └── ...               # Other helper modules

```

## Contributing

We welcome contributions to the Nice-Face project. To contribute, please follow these steps:

* 1. Fork the repository.
* 2. Create a new branch (git checkout -b feature-branch).
* 3. Make your changes and commit them (git commit -m 'Add new feature').
* 4. Push to the branch (git push origin feature-branch).
* 5. Create a new Pull Request.
* 6. Please ensure your code adheres to our coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License.
