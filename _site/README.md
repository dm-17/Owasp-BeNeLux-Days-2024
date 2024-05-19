OWASP BeNeLux Days

How to test pages locally

1/ Define the root folder:
- If you run locally, use `baseurl: "/"` in _config.yml 
- If you host it e.g. on github pages, set the folder in `baseurl: "foldername"` 

2/ Start the container with 
docker-compose up

3/ Open http://localhost:4000 in your favorite browser.
