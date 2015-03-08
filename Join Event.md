# Mini-Proyek-KPPL

<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Untitled Document</title>
<script type="text/javascript">
function MM_swapImgRestore() { //v3.0
  var i,x,a=document.MM_sr; for(i=0;a&&i<a.length&&(x=a[i])&&x.oSrc;i++) x.src=x.oSrc;
}
function MM_preloadImages() { //v3.0
  var d=document; if(d.images){ if(!d.MM_p) d.MM_p=new Array();
    var i,j=d.MM_p.length,a=MM_preloadImages.arguments; for(i=0; i<a.length; i++)
    if (a[i].indexOf("#")!=0){ d.MM_p[j]=new Image; d.MM_p[j++].src=a[i];}}
}

function MM_findObj(n, d) { //v4.01
  var p,i,x;  if(!d) d=document; if((p=n.indexOf("?"))>0&&parent.frames.length) {
    d=parent.frames[n.substring(p+1)].document; n=n.substring(0,p);}
  if(!(x=d[n])&&d.all) x=d.all[n]; for (i=0;!x&&i<d.forms.length;i++) x=d.forms[i][n];
  for(i=0;!x&&d.layers&&i<d.layers.length;i++) x=MM_findObj(n,d.layers[i].document);
  if(!x && d.getElementById) x=d.getElementById(n); return x;
}

function MM_swapImage() { //v3.0
  var i,j=0,x,a=MM_swapImage.arguments; document.MM_sr=new Array; for(i=0;i<(a.length-2);i+=3)
   if ((x=MM_findObj(a[i]))!=null){document.MM_sr[j++]=x; if(!x.oSrc) x.oSrc=x.src; x.src=a[i+2];}
}
</script>
</head>

<body onload="MM_preloadImages('Image/Home.png','Image/Event Gal 1.png','Image/About 1.png','Image/Login 1.png','Image/Sign up 1.png')">
<table width="100%" border="0">
  <tr>
    <th width="19" height="109" align="right" valign="middle"><table width="100%" border="0">
      <tr>
        <th width="19%" scope="col">&nbsp;</th>
        <th align="right" scope="col">Hi, Welcome! <a href="Login.php" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Login','','Image/Login 1.png',1)"><img src="Image/Login.png" alt="" width="130" height="21" id="Login" /></a><a href="Sign Up.php" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Sign Up','','Image/Sign up 1.png',1)"><img src="Image/Sign up.png" alt="" width="130" height="21" id="Sign Up" /></a></th>
        <th align="right" scope="col">&nbsp;</th>
      </tr>
    </table>
    <p><img src="Image/Logo.png" alt="" width="579" height="110" /></p></th>
  </tr>
</table>
<table width="100%" border="0">
  <tr>
    <td colspan="2" align="center" valign="middle"><a href="Index.php" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Home','','Image/Home.png',1)"><img src="Image/Home 1.png" alt="Home" width="180" height="38" id="Home" /></a><a href="Event Gallery.php" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Event Gal','','Image/Event Gal 1.png',1)"><img src="Image/Event Gal.png" alt="Event Gal" width="309" height="38" id="Event Gal" /></a><a href="Event.php" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Event','','Image/Event 1.png',0)"><img src="Image/Event.png" alt="Event" width="116" height="38" id="Event" /></a><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('About','','Image/About 1.png',1)"><img src="Image/About.png" alt="About" width="214" height="38" id="About" /></a><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Event Gal','','Image/Event Gal 1.png',1)"><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Event','','Image/Event 1.png',1)"></a><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('About','','Image/About 1.png',1)"></a></td>
    <td height="65" align="center" valign="middle">&nbsp;</td>
  </tr>
</table>
<table width="100%" border="0">
  <tr>
    <th height="87" align="center" scope="col">Submit Validation</th>
  </tr>
  <tr>
    <td height="48" align="center">Your time remining for submission : </td>
  </tr>
  <tr>
    <td align="right"><table width="100%" border="0">
      <tr>
        <th height="61" align="center" scope="col"><input name="Browse" type="file" id="Browse" size="80" /></th>
      </tr>
    </table>
      <form id="form1" name="form1" enctype="multipart/form-data" method="post" action="">
    </form></td>
  </tr>
</table>
<table width="89%" border="0">
  <tr>
    <th align="right" scope="col"><img src="Image/Submit.png" alt="" width="70" height="28" /></th>
  </tr>
</table>
<p>&nbsp;</p>
</body>
</html>
