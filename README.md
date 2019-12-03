# Spring Cloud Netflix
## Service Discovery

### Key Component
Discovery Server
Service
Client

# Spring Cloud Config
## Spring Cloud Config Server
### REST Endpoints

#### REST Endpoint Parameters
{application} spring.application.name on client
{profile} spring.profiles.active on client
{label} branch on server source

#### /{application}/{profile}[/{label}]
```
/evc-tob/test/master 
/evc-tob/prod/develop
/evc-tob/default
```

#### /{application}-{profile}.(yml | properties)
```
/evc-tob-test.yml
/evc-tob-prod.properties
/evc-tob-default.properties

```
#### /{label}/{application}-{profile}.(yml | properties)
```
• /master/evc-tob-master.yml
• /develop/evc-tob-prod.properties
• /master/evc-tob-default.properties

```

## Spring Cloud Config Client

### Config First
```
spring.application.name=evc_tob
spring.cloud.config.uri=http://localhost:8883/
```

### Discovery First
```
spring.application.name=evc_tob 
spring.cloud.config.discovery.enabled=true
```

## Updating Configuration at Runtime

### /refresh
@ConfigurationProperties

### @RefreshScope
add @RefreshScope will reinitialize @Value @Bean
