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