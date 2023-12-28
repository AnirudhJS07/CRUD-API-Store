# Installation Guide

This repository contains a Django REST Framework (DRF) project. It is designed to provide a tool for users to check the correctness of their sentences in various languages.

## Features

- User authentication and authorization using token-based authentication
- CRUD (Create, Read, Update, Delete) operations for different models
- API endpoints for accessing and manipulating data
- Integration with Django Admin for easy management of models
- 25 Different Language Models
- Output is a representation of Errors, Suggestions, and Corrected Sentence.

## Installation

To get started with the DRF project, follow these steps:

1. Clone the repository:
    `git clone https://github.com/AnirudhJS07/drf_project.git`
2. Navigate to the project directory:
    `cd drf_project`
3. Create and Activate Virtual Environment
    `python -m venv env`
4. Install Project Dependencies
    `pip install -r requirements.txt`
5. Apply Database Migrations
    `python manage.py migrate`
6. Start the development server
    `python manage.py runserver`
7. Access the API endpoints in your browser at `http://localhost:8000/`.

## Endpoints

- **Home / Overview Endpoint**
  - `/`: API overview providing general information about the available endpoints.

- **Box Endpoints**
  - `POST /box/create/`: Create a new box.
  - `GET /box/list/`: Retrieve a list of all boxes.
  - `GET /box/my_list/`: Retrieve a list of your own boxes.
  - `PUT /box/update/<str:pk>`: Update details of a specific box.
  - `DELETE /box/delete/<str:pk>`: Delete a specific box.

## Usage

You can use various tools such as cURL, Postman, or any other HTTP client to make requests to these endpoints and perform CRUD operations. Here's an example using cURL:

### Create a new box
```
curl -X POST http://your-api-url/box/create/ -d "length=10&breadth=5&height=3"
```

### Retrieve a list of all boxes
```
curl http://your-api-url/box/list/
```

### Retrieve a list of your own boxes
```
curl http://your-api-url/box/my_list/
```

### Update details of a specific box
```
curl -X PUT http://your-api-url/box/update/box_id -d "length=12&breadth=6&height=4"
```

### Delete a specific box
```
curl -X DELETE http://your-api-url/box/delete/box_id
```


## Contributing

Contributions to the DRF project are welcome! If you find any issues or want to add new features, please feel free to open a pull request. Make sure to follow the existing coding style and provide appropriate tests for your changes.
