# Node cookbook 🏠💻👩‍💻

•• Description

## List of what Installs:

• NodeJs

• Nginx

• pm2 and npm

## Commands

### Test Locally
- Running my unit test:

```
chef exec rspec
```
- Running integration tests and closing machine:

```
kitchen tests
```

## Tests in AWS
- Running integration tests in AWS

```
KITCHEN_YAML=kitchen_cloud.yml kitchen test
```
