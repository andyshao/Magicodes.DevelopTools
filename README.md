# Magicodes.DevelopTools   �����߹���

### Magicodes.CmdTools  �����и�������

#### copy	�����ļ�
	-s  Դ·�������
	-t	Ŀ��·�������
	-c	�����ļ�·��
    -i  ���Ե��ļ���&��չ��&Ŀ¼����������÷ֺŷָ
	-d	����ģʽ��Ĭ��false


#### order	�ı�����
	-s  Դ·�������
	-t	Ŀ��·��

#### replace	�滻�ļ����ı�
	-p  Ŀ¼���ļ�·�������
	-s  Դ�ַ�����������Կո�ָ��������
	-t	Ŀ���ַ�����������Կո�ָ��������
    -i  �Ƿ��滻�ı�(bool)


#### Demo:

	call "tools/Magicodes.CmdTools.exe" order -s "changeList.txt"
	���ļ�"changeList.txt"�ڵ��ı��������򣬲�ȥ���ظ����Լ���β�ո�

	call "tools/Magicodes.CmdTools.exe" copy -s "../../Magicodes.Admin" -t "../" -c "changeList.txt"
	��������"changeList.txt"��"../../Magicodes.Admin"Ŀ¼�����ļ���"../"Ŀ¼

    call "$(SolutionDir)tools\tools\Magicodes.CmdTools.exe" copy -i ".cs" -s "$(SolutionDir)plus\Magicodes.Test\Magicodes.Test.Web.Mvc\Views" -t "$(SolutionDir)src\Magicodes.Admin.Web.Mvc\wwwroot\PlugIns\Magicodes.Test.Web.Mvc\Views"
    �˴�����������VS�����ļ��������¼�֮�У��������ɳɹ�ʱ��������ļ������Ŀ¼�����︴����ͼ�����Ŀ¼���Һ������ļ�

    call "Magicodes.CmdTools.exe" replace -s "Magicodes.Test Test" -t "$(companyName).$(projectName) $(projectName)" -p "./tps" -i true
    ���ַ���Magicodes.Test��Test�������ļ����еĴ��ַ������滻Ϊ$(companyName).$(projectName)��$(projectName)���滻Ŀ¼Ϊ��ǰĿ¼�µ�tpsĿ¼�µ������ļ���Ŀ¼�Լ��ļ�����

    call "Magicodes.CmdTools.exe" replace -s "<#=modelTypeNameSpace#> <#=tPrimaryKey#> <#=modelTypeVarName#> <#=repositoryName#> businessPropertys" -t "<#=host.ModelLastNameSpace#> <#=host.PrimaryKeyShortTypeName#> <#=host.ModelVarName#> <#=host.RepositoryVarName#> host.BusinessProperties" -p "./tps/ModelProject" -i true
    ���ַ���<#=modelTypeNameSpace#>��<#=tPrimaryKey#>��<#=modelTypeVarName#>��<#=repositoryName#> ��businessPropertys�������ļ����еĴ��ַ������滻Ϊ<#=host.ModelLastNameSpace#>��<#=host.PrimaryKeyShortTypeName#>��<#=host.ModelVarName#>��<#=host.RepositoryVarName#>��host.BusinessProperties���滻Ŀ¼Ϊ��ǰĿ¼�µ�tps/ModelProjectĿ¼�µ������ļ���Ŀ¼�Լ��ļ�����