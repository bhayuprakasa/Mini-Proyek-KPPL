# Mini-Proyek-KPPL

<?php //virtual('/Connections/koneksi.php'); ?>
<?php
if (!function_exists("GetSQLValueString")) {
function GetSQLValueString($theValue, $theType, $theDefinedValue = "", $theNotDefinedValue = "") 
{
  if (PHP_VERSION < 6) {
    $theValue = get_magic_quotes_gpc() ? stripslashes($theValue) : $theValue;
  }

  $theValue = function_exists("mysql_real_escape_string") ? mysql_real_escape_string($theValue) : mysql_escape_string($theValue);

  switch ($theType) {
    case "text":
      $theValue = ($theValue != "") ? "'" . $theValue . "'" : "NULL";
      break;    
    case "long":
    case "int":
      $theValue = ($theValue != "") ? intval($theValue) : "NULL";
      break;
    case "double":
      $theValue = ($theValue != "") ? doubleval($theValue) : "NULL";
      break;
    case "date":
      $theValue = ($theValue != "") ? "'" . $theValue . "'" : "NULL";
      break;
    case "defined":
      $theValue = ($theValue != "") ? $theDefinedValue : $theNotDefinedValue;
      break;
  }
  return $theValue;
}
}

$editFormAction = $_SERVER['PHP_SELF'];
if (isset($_SERVER['QUERY_STRING'])) {
  $editFormAction .= "?" . htmlentities($_SERVER['QUERY_STRING']);
}

if ((isset($_POST["MM_insert"])) && ($_POST["MM_insert"] == "form1")) {
  $insertSQL = sprintf("INSERT INTO `sign up` (`First Name`, `Last Name`, Username, Email, Password, `Confirm Password`) VALUES (%s, %s, %s, %s, %s, %s)",
                       GetSQLValueString($_POST['First_Name'], "text"),
                       GetSQLValueString($_POST['Last_Name'], "text"),
                       GetSQLValueString($_POST['Username'], "text"),
                       GetSQLValueString($_POST['Email'], "text"),
                       GetSQLValueString($_POST['Password'], "text"),
                       GetSQLValueString($_POST['Confirm_Password'], "text"));

  mysql_select_db($database_koneksi, $koneksi);
  $Result1 = mysql_query($insertSQL, $koneksi) or die(mysql_error());

  $insertGoTo = "Succes Sign Up.html";
  if (isset($_SERVER['QUERY_STRING'])) {
    $insertGoTo .= (strpos($insertGoTo, '?')) ? "&" : "?";
    $insertGoTo .= $_SERVER['QUERY_STRING'];
  }
  header(sprintf("Location: %s", $insertGoTo));
}

if ((isset($_POST["MM_insert"])) && ($_POST["MM_insert"] == "form2")) {
  $insertSQL = sprintf("INSERT INTO `sign up` (`First Name`, `Last Name`, Username, Email, Password, `Confirm Password`) VALUES (%s, %s, %s, %s, %s, %s)",
                       GetSQLValueString($_POST['First_Name'], "text"),
                       GetSQLValueString($_POST['Last_Name'], "text"),
                       GetSQLValueString($_POST['Username'], "text"),
                       GetSQLValueString($_POST['Email'], "text"),
                       GetSQLValueString($_POST['Password'], "text"),
                       GetSQLValueString($_POST['Confirm_Password'], "text"));

  mysql_select_db($database_koneksi, $koneksi);
  $Result1 = mysql_query($insertSQL, $koneksi) or die(mysql_error());
}
?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Untitled Document</title>
<style type="text/css">
body,td,th {
	color: #090;
	font-size: 24px;
	font-family: Arial, Helvetica, sans-serif;
	position: relative;
}
body {
	margin-right: 0cm;
}
</style>
<script type="text/javascript">
function MM_preloadImages() { //v3.0
  var d=document; if(d.images){ if(!d.MM_p) d.MM_p=new Array();
    var i,j=d.MM_p.length,a=MM_preloadImages.arguments; for(i=0; i<a.length; i++)
    if (a[i].indexOf("#")!=0){ d.MM_p[j]=new Image; d.MM_p[j++].src=a[i];}}
}
function MM_swapImgRestore() { //v3.0
  var i,x,a=document.MM_sr; for(i=0;a&&i<a.length&&(x=a[i])&&x.oSrc;i++) x.src=x.oSrc;
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

<body onload="MM_preloadImages('Image/Home.png','Image/Event Gal 1.png','Image/Event 1.png','Image/About 1.png','Image/Login 1.png','Image/Sign up 1.png')">
<table width="100%" border="0">
  <tr>
    <th width="19" height="109" align="right" valign="middle"><img src="Image/Logo.png" width="579" height="110" /></th>
  </tr>
  <tr>
    <td height="65" align="center" valign="middle"><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Home','','Image/Home.png',1)"><img src="Image/Home 1.png" width="180" height="38" id="Home" /></a><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Event Gal','','Image/Event Gal 1.png',1)"><img src="Image/Event Gal.png" width="309" height="38" id="Event Gal" /></a><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('Event','','Image/Event 1.png',1)"><img src="Image/Event.png" width="116" height="38" id="Event" /></a><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('About','','Image/About 1.png',1)"><img src="Image/About.png" alt="" width="214" height="38" id="About" /></a><a href="#" onmouseout="MM_swapImgRestore()" onmouseover="MM_swapImage('About','','Image/About 1.png',1)"></a></td>
  </tr>
</table>
<form action="<?php echo $editFormAction; ?>" method="post" name="form2" id="form2">
  <table width="504" height="323" align="center">
    <tr valign="baseline">
      <td width="203" align="right" nowrap="nowrap">First Name:</td>
      <td width="233"><input type="text" name="First_Name" value="" size="32" /></td>
    </tr>
    <tr valign="baseline">
      <td nowrap="nowrap" align="right">Last Name:</td>
      <td><input type="text" name="Last_Name" value="" size="32" /></td>
    </tr>
    <tr valign="baseline">
      <td nowrap="nowrap" align="right">Username:</td>
      <td><input type="text" name="Username" value="" size="32" /></td>
    </tr>
    <tr valign="baseline">
      <td nowrap="nowrap" align="right">Email:</td>
      <td><input type="text" name="Email" value="" size="32" /></td>
    </tr>
    <tr valign="baseline">
      <td nowrap="nowrap" align="right">Password:</td>
      <td><input type="password" name="Password" value="" size="32" /></td>
    </tr>
    <tr valign="baseline">
      <td nowrap="nowrap" align="right">Confirm Password:</td>
      <td><input type="password" name="Confirm_Password" value="" size="32" /></td>
    </tr>
    <tr valign="baseline">
      <td nowrap="nowrap" align="right">&nbsp;</td>
      <td><input type="submit" value="Sign Up" /></td>
    </tr>
  </table>
  <input type="hidden" name="MM_insert" value="form2" />
</form>
<p>&nbsp;</p>
<p>&nbsp;</p>
</body>
</html>
