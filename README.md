# aws-minecraft

## Goals

- [x] Full infrastructure-as-code configuration,
- [x] An auto-starting Minecraft server,
- [ ] S3 storage to persist the server,
- [ ] Auto-archive backups to S3,
- [x] Resilient hosting capability on [spot instances](https://aws.amazon.com/ec2/spot/),

## Stretch Goals

- [ ] Multiple servers on a single instance,
- [ ] Cleaner variable usage

## Configuration

- Create the S3 bucket
- Pre-seed S3 with the desired server JAR and any configuration files:

  ```sh
  aws s3 cp server.jar s3://${var.s3_bucket}/server/server.jar
  aws s3 cp ops.txt    s3://${var.s3_bucket}/server/ops.txt
  # ...
  ```
