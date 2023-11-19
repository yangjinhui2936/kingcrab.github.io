---
title: ���ʹ��mkcdoc��github�ϲ���̬��վ
hide:
  - toc
---

* ͨ��github/gitee page������ҳ���������foam/obsidian/markdown�ʼǣ�
* ʡ��һ�������obsidian publish��8����/��

[English Version](https://github.com/Jackiexiao/foam-mkdocs-template/blob/master/README.md)

Ū��֮�������վ��������ӣ�
![foam-mkdocs-template-png](demo-mkdocs.png)


## ����

* [github page](https://jackiexiao.github.io/foam-mkdocs-template/)
* ���ڷ���[gitee page](https://jackiegeek.gitee.io/foam-mkdocs-template/)

## ʹ�÷���������github page���ɲ�����վ

1. ����Fork������������ֿ�
2. ���� `.github  mkdocs.yml requirements.txt` ����Ĳֿ����棬�½�һ�� docs �ļ���
3. ������ĵ���ӵ�`docs`���棨ԭ�����ļ�����ȫ��ɾ��������`docs`�����һ��`index.md`��Ϊ��վ��ҳ�������У�
4. ����`mkdocs.yml`�޸�`site_name`Ϊ�����վ���ƣ�����ļ�����������վ�����ã��������ý̳̼���������ʹ��Ĭ�����ã������ˣ���ʱ�����Լ����ڣ���
* [mkdocs-material](https://squidfunk.github.io/mkdocs-material/)
* [mkdocs](https://www.mkdocs.org/user-guide/configuration/)
5. push�ύ�޸ĵ�github
6. �����github�ֿ�-setting������github page��ѡ���֧-gh-pages����һС�ᣬ�ͻ�����ַ���������ҵ���`jackiexiao.github.io/blog/`
7. �󹦸�ɣ�

֮����git push�Ϳ����Զ�������ҳ�����ɲ��ͣ�����Ϊgithub action�������ã�����Ȥ�����Լ�����һ�¡�

## ͬ��������Gitee page���ٹ��ڷ���

����ܼ򵥣��������[����](https://jackiegeek.gitee.io/blog/)����Gitee����ҳ���½��ֿ⣬��ҳ���·�ѡ��`�������вֿ�`, ��д���github�ֿ��ַ��Ȼ����`����`->`Gitee Page`->`�����֧`->ѡ��`gh-pages`�����`����`��������������ˢ����Ϳ��Կ����Լ�gitee apge�������ˡ�����Ҫע����ǣ�ÿ�θ���Gitee page������Ҫ3������

1. �������github�ֿ�
2. ��Gitee���ֶ����ͬ��github
3. ��ǰ��Ĳ��裬�ٴβ���Gitee Page 

## ���ز���

�����Եģ�������Ҫ���ز����ĵ���������Ƶ�����޸ĺ�Ԥ������򵥵ķ����ǽ�������ļ��У��ֿⱾ�ص�ַ��Ҳ����`docs`�ļ��е���һ���������python��Ҫ3.6����
```
pip install -U -r requirements.txt
mkdocs serve 
```
Ȼ�����`http://127.0.0.1:8000/`�Ϳ�����

## ����

���ģ��ʹ�õĿ�
* [mkdocs](https://www.mkdocs.org/user-guide/configuration/)
* [mkdocs-material](https://squidfunk.github.io/mkdocs-material/)
* [mkdocs-roamlinks-plugin](https://github.com/Jackiexiao/mkdocs-roamlinks-plugin)

## ֧�ֵ��﷨
���ģ��Ὣmarkdown�е����ӽ�������ҳ֧�ֵĸ�ʽ��֧�ֵĸ�ʽ����

| ԭʼ                  | ת����                             |
| ----------------------- | ----------------------------------- |
| `[Git Flow](git_flow.md)` | `[Git Flow](../software/git_flow.md)` |
| `[[Git Flow]]`            | `[Git Flow](../software/git_flow.md)` |
| `![[image.png]]`           | `![image.png](../image/imag.png)`      |
| `[[#Heading identifiers]]` | `[Heading identifiers in HTML](#heading-identifiers-in-html)`
| ` [[Git Flow#Heading]]` | `[Git Flow](../software/git_flow.md#heading)` |
