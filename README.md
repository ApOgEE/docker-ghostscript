# Ghostscript Docker Image

### Example Ghostscript to reduce PDF size

we can use ghostscript to reduce pdf size

before...
```
$ du -h file.pdf
27M file.pdf
```

Example command to run
```
$ docker run --rm $(pwd):/root apogeek/gs gs -sDEVICE=pdfwrite -dPDFSETTINGS=/ebook -q -o output.pdf file.pdf
```

after...
```
$ du -h output.pdf
900K    output.pdf
```
