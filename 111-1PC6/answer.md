# 第6次練習-練習-PC6
>
>學號：109111101 
><br />
>姓名：邱韋翔
><br />
>作業撰寫時間：3 (mins，包含程式撰寫時間)
><br />
>最後撰寫文件日期：2022/11/07
>

本份文件包含以下主題：(至少需下面兩項，若是有多者可以自行新增)
- [x]說明內容
- [x]個人認為完成作業須具備觀念

## 說明程式與內容

拉取工具箱中的下拉式選單也就是`DropDownList`
下段程式碼則為使用後結果：

```html
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Test.aspx.cs" Inherits="_111_1PC6.Test" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <title></title>
</head>
<body>
    <form id="form1" runat="server">
        <div>
            <asp:DropDownList ID="ddl_Test" runat="server"></asp:DropDownList>
        </div>
    </form>
</body>
</html>
```
給予一個String型別的list，運用for迴圈給DropDownList下拉式選單添加選項，
在運用DropDownList.SelectIndex抓取選的值，讓操作者點選下拉式選單有選項選擇。
下段程式碼則為使用後結果：

```csharp
public partial class Test : System.Web.UI.Page
    {
        string[] sa_School = new string [3] { "台科", "北科", "亞東" };
        protected void Page_Load(object sender, EventArgs e)
        {
            for (int i_Ct = 0; i_Ct<sa_School.Length; i_Ct++)
            {
                ListItem o_L = new ListItem();
                o_L.Text = sa_School[i_Ct];
                o_L.Value = sa_School[i_Ct];
                ddl_Test.Items.Add(o_L);
            }
            
        }
    }
```


## 個人認為完成作業須具備觀念

須了解DropDownList的物件控制，給予對應控制物件的指令即可

