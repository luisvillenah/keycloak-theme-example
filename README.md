# Keycloak Theme Development

This is a Keycloak Server image for theme development.

## Usage

Use `KEYCLOAK_USER` and `KEYCLOAK_PASSWORD` environment variables to set the admin user credentials the first time you boot the server.

```
docker-compose build
KEYCLOAK_USER=<admin_user> KEYCLOAK_PASSWORD=<admin_password> docker-compose up
```

By default the port 8080 mapped locally, visit http://localhost:8080 to access the admin console.

# Creating a theme

Follow the [Server Development](https://www.keycloak.org/docs/6.0/server_development/#configure-theme) guide to extend and customize the base theme. By default every theme type extends the keycloak theme, consider to extend the base theame instad.

Add your files in the `theme` directory.

**Note**: You have to restart the server to reload the parent theme. Template cache is disabled, you don't need to restart the server to reload templates.