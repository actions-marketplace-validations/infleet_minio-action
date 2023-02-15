# MinIO Github Action

This [GitHub Action](https://github.com/features/actions) sets up MinIO instance.

Docker images source [minio/minio](https://hub.docker.com/r/minio/minio).

---

# Usage

See [action.yml](action.yml)

Basic:

```yaml
- name: Start UP MinIO
  uses: infleet/minio-action@v0.0.1
  with:
    port: "9000"
    version: "latest"
    username: "minio"
    password: "minio"
```

Now you should be able to connect to `MinIO` (S3 api) running at `localhost:9000`

---

## Configurations

| Name       | Default  | Required? | Description                                                                         |
| ---------- | -------- | :-------: | ----------------------------------------------------------------------------------- |
| `version`  | `latest` |    [ ]    | Version of MinIO                                                                    |
| `port`     | `9000`   |    [ ]    | Port to forward the access to MinIO, S3 API like                                    |
| `username` |          |    [x]    | The username used to authenticate to S3 api, common used as `AWS_ACCESS_KEY_ID`     |
| `password` |          |    [x]    | The password used to authenticate to S3 api, common used as `AWS_SECRET_ACCESS_KEY` |
