# aws-glue-libs

https://github.com/awslabs/aws-glue-libs をフォークしたものです。

# requirements
- jdk8
- pyenv
- direnv

# Setup
1. bash setup_glue2.0.sh # MavenとSparkインストール
2. pyenv install         # python 3.7.12インストール
3. direnv allow          # ENVIRONMENT設定
4. bin/gluesparksubmit {{SCRIPT}} --JOB_NAME={{ANYNAME}} [--OPTIONS]

# Configuration
spark設定を直接追加する時は、conf/spark-customs.confにて内容を追加します。
```
#spark.hadoop.fs.s3a.endpoint http://localhost:9000         # for local s3 endpoint(minio)
spark.hadoop.fs.s3a.path.style.access true                  # for s3 access
spark.hadoop.fs.s3a.signing-algorithm S3SignerType          # for s3 access
fs.s3.impl org.apache.hadoop.fs.s3native.NativeS3FileSystem # for s3 access
#spark.driver.memory 4g                                     # default: 1g
#spark.executor.memory 4g                                   # default: 1g
```