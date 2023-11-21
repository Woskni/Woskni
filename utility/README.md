
## CSVLoader.cs
### �T�v
- CSV�t�@�C�����O������ǂݍ��ލۂɗp����N���X�ł�

### �֐�
- �R���X�g���N�^: �t�@�C���p�X���w�肵��CSV�t�@�C����ǂݍ��݂܂�
- `GetString`�֐�: ���� `row`, `col` ���當������擾���܂�
- `GetInteger`�֐�: ���� `row`, `col` ���琮�����擾���܂�
- `GetFloat`�֐�: ���� `row`, `col` ����������擾���܂�
- `Find`�֐�: �f�[�^�̍��W���������AVector2Int�^�ŕԂ��܂�

<br></br>

## EditorTheme.cs

### �񋓌^
- `ThemeType`: �t�@�C���p�X�̊J�n�ʒu���ł�
    > `Right`: ���C�g�e�[�}
    > `Dark`: �_�[�N�e�[�}

### �T�v
- Unity�̃G�f�B�^�e�[�}�u���C�g�e�[�}�v�u�_�[�N�e�[�}�v�Ɋ֘A����w�i�F�E�A�C�R���F�̎擾���s���N���X�ł�

### �ϐ�
- `lightThemeColor`: ���C�g�e�[�}�̔w�i�F�ł�
- `lightIconColor`: ���C�g�e�[�}�̃A�C�R���F�ł�
- `darkThemeColor`: �_�[�N�e�[�}�̔w�i�F�ł�
- `darkIconColor`: �_�[�N�e�[�}�̃A�C�R���F�ł�
- `theme`: �G�f�B�^�e�[�}�̎�ނ�񋓌^`EditorTheme.ThemeType`�ŕԂ��܂�

### �֐�
- `GetThemeColor`�֐�: ���݂̃e�[�}�̔w�i�F��Ԃ��܂�
- `GetIconColor`�֐�: ���݂̃e�[�}�̃A�C�R���F��Ԃ��܂�

<br></br>

## MeshCombiner.cs
### �T�v
- ���b�V���̌������s���N���X�ł�

### �֐�
- `Combine`�֐�
    - ���b�V���̌������s���܂�
        > ������`gameObjects`: ��������I�u�W�F�N�g  
        > ������`name`: ������̃I�u�W�F�N�g�̖��O  
        > ��O����`parent`: ������̃I�u�W�F�N�g�̐e

<br></br>

## PathConverter.cs
### �T�v
- �t�@�C���p�X��ϊ�����N���X�ł�

### �񋓌^
- `FilePathType`: �t�@�C���p�X�̊J�n�ʒu���ł�
    > `RootDirectoryPath`: ���[�g�f�B���N�g������̐�΃p�X
    > `AssetsPath`: �v���W�F�N�g�Ȃ�
    > `CurrentDirectoryPath`: 

### �֐�
- `Combine`�֐�
    - ���b�V���̌������s���܂�
        > ������`gameObjects`: ��������I�u�W�F�N�g  
        > ������`name`: ������̃I�u�W�F�N�g�̖��O  
        > ��O����`parent`: ������̃I�u�W�F�N�g�̐e

