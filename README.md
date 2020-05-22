# The Mental Wellbeing Project Website

This is the website of our mental wellbeing project.

This website is powered by Jekyll and some Bootstrap, Bootwatch. Go to 
*aboutwebsite.md*  to learn how to copy and modify this page for your purpose. 


A big thank you to https://github.com/mpa139/allanlab for setting up this 
framework.


### For development

1. Install docker
2. Fork and clone this repo
3. 

```
docker run -it --rm --volume="$(pwd):/srv/jekyll" \
 --volume="$(pwd)/vendor/bundle:/usr/local/bundle" \
 --env JEKYLL_ENV=development -p 4000:4000 \
 jekyll/jekyll:4.0.1 jekyll serve
```