# Strapi Docker Compose
## Usage 
- Modify the `volumes:` section of the docker compose file to change the generated src location
- `docker-compose up -d`
- Wait for 5-10 minutes for the application to spin up
- Check on the status by executing `docker logs -f <container-id>`
- Navigate to `http://localhost:8080/`
- And the admin page at `http://localhost:8080/admin`
- Create a user with username password and email
- Go to the `http://localhost:8080/admin/plugins/upload` page and upload a test file
- Navigate to the file similar to `http://localhost:8080/uploads/<file-id>`
- Next navigate to [content type builder](http://localhost:8080/admin/plugins/content-type-builder)
- Create a content type like `blog` and add a `String` field, a `Text` field, and a `Date` field
- Next navigate to the Blog Content Type and add a new blog.
- Navigate to the `Roles & Permissions` Plugin and Click the `Public` role
  - Under Permissions, click and expand `APPLICATION` and set the permissions for the newly created content type. 
  - For now set `count`, `find`, and `findone`
- Now you can navigate to `localhost:8080/blogs` to query the blogs content.
- Check the [documentation](https://strapi.io/documentation/3.0.0-beta.x/content-api/api-endpoints.html) for help on querying the api.
- Continue learning using the [tutorial](https://strapi.io/documentation/3.0.0-beta.x/getting-started/quick-start-tutorial.html)