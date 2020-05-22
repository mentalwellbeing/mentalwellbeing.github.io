# The Mental Wellbeing Project Website

This is the website of our mental wellbeing project.

This website is powered by Jekyll and some Bootstrap, Bootwatch. Go to 
*aboutwebsite.md*  to learn how to copy and modify this page for your purpose. 


A big thank you to https://github.com/mpa139/allanlab for setting up this 
framework.


### For development

1. Install docker
2. Fork and clone this repo
3. Run docker in the cloned directory using this command. Note that if you
run into a bundler error you may need to delete Gemfile.lock 

```
docker run -it --rm --volume="$(pwd):/srv/jekyll" \
 --volume="$(pwd)/vendor/bundle:/usr/local/bundle" \
 --env JEKYLL_ENV=development -p 4000:4000 \
 jekyll/minimal:4.0.1 jekyll serve
```
4. Open http://localhost:4000/ in your browser. The site won't refresh but the 
backend will update as you change your files.
