XML
===

//载入一个XML文档
xmldocument doc=new xmldocument();
string path="student.xml";
doc.load(path);
//保存于新的文档中
doc.save("student1.xml");
//得到文档的根节点
xmlnode root=doc.GetElement;
//得到第一个子节点
xmlnode childnode=root.firstchild;
//获取子节点的属性值
xmlElement xe=(xmlElement)childnode;
string id=xe.GetAttribute("id");
//获取文档中所有节点的属性值
xmlNodeList list =root.childnodes;
List<string> list1=new List<string> ();
foreach(xmlElement xe1 in list)
{
  string s= xe1.GetAttribute("id");
  list1.add(s);
}

//创建一个新节点
xmlElement stuXE=doc.createElement("stu");
root.AppendChild(stuXE);
string id="";
stuXE.setAttribute("id",id);
//找到一个节点
string id="";//input id
string xpath="//stu[@id='{0}']";
xpath=string.format(xpath,id);
xmlNode node=doc.selectSingleNode(xpath);
