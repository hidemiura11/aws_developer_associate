## AWS CLI commands for Secrets Manager
# �V�[�N���b�g�̈ꗗ�\��
aws secretsmanager list-secrets
# �V�[�N���b�g�̍쐬
aws secretsmanager create-secret --name database-secret --secret-string "PassForRDS"
# �V�[�N���b�g�̎擾
aws secretsmanager get-secret-value --secret-id database-secret
# �V�[�N���b�g�̍X�V
aws secretsmanager update-secret --secret-id database-secret --secret-string "NewPassForRDS"
# �V�[�N���b�g�̍폜
aws secretsmanager delete-secret --secret-id database-secret