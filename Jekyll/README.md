
## Jekyll

A basic container with Jekyll developement environment setup.

---

### Image

Docker image is hosted [here](https://hub.docker.com/r/prakashr1984/jekyll/)

---

### Usage


    docker run --rm -v "$PWD:/src" grahamc/jekyll build

or for repeated calls:

    alias jekyll='docker run -it --rm -p 4000:4000 -v "$(pwd):/src" jekyll jekyll serve -H 0.0.0.0'
    jekyll build
    jekyll serve -H 0.0.0.0

run as a background daemon:

    docker run -it -d -p 4000:4000 -v "$(pwd):/src" jekyll jekyll serve -H 0.0.0.0
    
---
*Thanks to [grahamc/jekyll](https://hub.docker.com/r/grahamc/jekyll/)*