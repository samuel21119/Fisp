# Fisp

Modern HTTP **F**ile **I**ndexer for **S**tatic **P**age.


![Icon](images/logo.png)

This project is use for static page hosting file indexer, such as github pages.  
Demo: [https://samuel.nctu.me/fisp](https://samuel.nctu.me/fisp)

![Screenshot](images/demo.png)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a static page.

### Prerequisites
- Your files
- Static page hosting service (ex. Github Pages)

### Installation
Copy `index.html` to every folder,
and generate `file.json` in every folder. (Instructions in [usage](#usage))

## Running the tests
It's suggested that testing this project with a file hosting server. Due to CORS policy, the website can't fetch `file.json` with XMLHttpRequest if simpily open `index.html` from file explorer.  
For example, use a python simple HTTP server:  
`$ python -m SimpleHTTPServer`

## Usage
After copied `index.html` to every folder, we need `file.json` in every folder too, in order make it be able to recognize which files is located in this directory.  
The file `file.json` is an array, consisting different objects, each representing a file or folder. It may look like this:  
```json
[
    {"type": "folder",
     "name": ".."},
    {"type": "word",
     "name": "Word.docx"},
    {"type": "ppt",
     "name": "presentation.pptx"}
]
```
Every objects have two data, *type* and *name*, if the *type* is one of the following one, webpage will display a specific icon, otherwise, it'll display *file* icon.

| Type | Icon |
| ------ | ----------- |
| word | <img src="images/word.png" width="30"> |
| ppt | <img src="images/ppt.png" width="30"> |
| excel | <img src="images/excel.png" width="30"> |
| video | <img src="images/video.png" width="30"> |
| pdf | <img src="images/pdf.png" width="30"> |
| image | <img src="images/image.png" width="30"> |
| code | <img src="images/code.png" width="30"> |
| audio | <img src="images/audio.png" width="30"> |
| file | <img src="images/file.png" width="30"> |
| folder | <img src="images/folder.png" width="30"> |

See [docs](https://github.com/samuel21119/fisp/tree/master/docs) for more details about `file.json`.


## Todo
 - [] Write `file.json` generator.

## Built With

* HTML 5 and CSS 5
* [FontAwesome](https://fontawesome.com/) - File types icons.

## Author

* [Samuel Huang (黃恩明)](https://samuel.nctu.me)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

















