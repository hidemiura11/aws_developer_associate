## AWS CLI commands for Secrets Manager
# シークレットの一覧表示
aws secretsmanager list-secrets
# シークレットの作成
aws secretsmanager create-secret --name database-secret --secret-string "PassForRDS"
# シークレットの取得
aws secretsmanager get-secret-value --secret-id database-secret
# シークレットの更新
aws secretsmanager update-secret --secret-id database-secret --secret-string "NewPassForRDS"
# シークレットの削除
aws secretsmanager delete-secret --secret-id database-secret