## Spring Cloud 

## Spring Cloud Netflix
Netflix OSS + Spring + Spring Boot

## Discovering Services With Spring Cloud

## Spring Cloud Config Server
### REST Endpoints

#### REST Endpoint Parameters
{application} maps to spring.application.name on client
{profile} maps to spring.profiles.active on client
{label} server side feature to refer to set of config files by name

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

## Updating Configuration at Runtime
