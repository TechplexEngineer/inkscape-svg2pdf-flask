# Inkscape as a service

A simple web service that transforms the given SVG file PDF. 

Run with `docker run -p 8080:8080 gcr.io/as-a-service-dev/inkscape`

### URL parameters:

* `input`: URL of the document to transform.

## Running the server locally

* Build with `docker build . -t inkscape`
* Start with `docker run -p 8080:8080 inkscape`
* Open in your browser at `http://localhost:8080/?url=https://upload.wikimedia.org/wikipedia/commons/f/fd/Ghostscript_Tiger.svg`

## Convert svg to pdf via curl

### Local File
`curl -o test.pdf --form file=@sample.svg http://localhost:8080/`

### Remote File
`curl -o test.pdf http://localhost:8080/?url=https://upload.wikimedia.org/wikipedia/commons/f/fd/Ghostscript_Tiger.svg`