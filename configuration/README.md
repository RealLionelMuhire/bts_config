# Bus Ticketing System Configuration

This repository contains centralized configurations for the Bus Ticketing System microservices.

## Structure

Each service has three configuration files:
- `{service-name}.yml`: Default configuration
- `{service-name}-dev.yml`: Development environment configuration
- `{service-name}-docker.yml`: Docker environment configuration

## Environment Variables

The following environment variables are used across configurations:

### Database
- `DB_HOST`: Database host
- `DB_PORT`: Database port (default: 5432)
- `DB_NAME`: Database name
- `DB_USERNAME`: Database username
- `DB_PASSWORD`: Database password

### Service Registry
- `EUREKA_HOST`: Eureka server host
- `EUREKA_PORT`: Eureka server port (default: 8081)

### Keycloak
- `KEYCLOAK_ISSUER_URI`: Keycloak issuer URI
- `KEYCLOAK_JWK_SET_URI`: Keycloak JWK set URI

### Config Server
- `CONFIG_SERVER_PASSWORD`: Config server authentication password

## Security

All sensitive information is stored as environment variables and should never be committed to this repository.

## Adding New Services

To add a new service configuration:
1. Create three configuration files following the naming convention
2. Use environment variables for sensitive information
3. Include appropriate logging levels for each environment
4. Configure service-specific settings
5. Test the configuration with the service

## Best Practices

1. Always use environment variables for sensitive data
2. Keep configurations minimal and specific to each environment
3. Use appropriate logging levels for each environment
4. Document any service-specific configurations
5. Test configurations before committing 