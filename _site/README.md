OWASP BeNeLux Days

How to test pages locally

1/ (No change needed anymore, you can skip to 2/)
When running this site in your own Github Pages repository, add a variable in GH "baseurl" with, as value, the base url of your repo.
Define the root folder:
- If you run locally, use `baseurl: "/"` in _config.yml
- If you host it e.g. on github pages, set the value of the baseurl in the environment variable to avoid issues.

2/ Start the container with 
docker-compose up

3/ Open http://localhost:4000 in your favorite browser.
