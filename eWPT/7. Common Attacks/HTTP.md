HTTP MEthod Tampering

:1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 3169  bytes 2874615 (2.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 3169  bytes 2874615 (2.7 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


┌──(root㉿INE)-[~]
└─# dirb http://192.190.82.3/

-----------------
DIRB v2.22    
By The Dark Raver
-----------------

START_TIME: Mon Sep 29 19:38:05 2025
URL_BASE: http://192.190.82.3/
WORDLIST_FILES: /usr/share/dirb/wordlists/common.txt

-----------------

GENERATED WORDS: 4612                                                          

---- Scanning URL: http://192.190.82.3/ ----
+ http://192.190.82.3/.git/HEAD (CODE:200|SIZE:23)                                                                                                                                        
+ http://192.190.82.3/cgi-bin/ (CODE:403|SIZE:210)                                                                                                                                        
==> DIRECTORY: http://192.190.82.3/css/                                                                                                                                                   
==> DIRECTORY: http://192.190.82.3/img/                                                                                                                                                   
+ http://192.190.82.3/index.php (CODE:200|SIZE:4408)                                                                                                                                      
==> DIRECTORY: http://192.190.82.3/js/                                                                                                                                                    
+ http://192.190.82.3/LICENSE (CODE:200|SIZE:10273)                                                                                                                                       
==> DIRECTORY: http://192.190.82.3/mail/                                                                                                                                                  
+ http://192.190.82.3/phpinfo.php (CODE:200|SIZE:74357)                                                                                                                                   
+ http://192.190.82.3/server-status (CODE:403|SIZE:215)                                                                                                                                   
==> DIRECTORY: http://192.190.82.3/uploads/                                                                                                                                               
==> DIRECTORY: http://192.190.82.3/vendor/                                                                                                                                                
                                                                                                                                                                                          
---- Entering directory: http://192.190.82.3/css/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.                        
    (Use mode '-w' if you want to scan it anyway)
                                                                                                                                                                                          
---- Entering directory: http://192.190.82.3/img/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.                        
    (Use mode '-w' if you want to scan it anyway)
                                                                                                                                                                                          
---- Entering directory: http://192.190.82.3/js/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.                        
    (Use mode '-w' if you want to scan it anyway)
                                                                                                                                                                                          
---- Entering directory: http://192.190.82.3/mail/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.                        
    (Use mode '-w' if you want to scan it anyway)
                                                                                                                                                                                          
---- Entering directory: http://192.190.82.3/uploads/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.                        
    (Use mode '-w' if you want to scan it anyway)
                                                                                                                                                                                          
---- Entering directory: http://192.190.82.3/vendor/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.                        
    (Use mode '-w' if you want to scan it anyway)
                                                                               
-----------------
END_TIME: Mon Sep 29 19:38:07 2025
DOWNLOADED: 4612 - FOUND: 6

┌──(root㉿INE)-[~]
└─# curl http://192.190.82.3                                                                                                                                                               

<!DOCTYPE html>
<html lang="en">

<head>

  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <meta name="description" content="">
  <meta name="author" content="">

  <title>Attack Defense Demo Blog</title>

  <!-- Bootstrap core CSS -->
  <link href="vendor/bootstrap/css/bootstrap.min.css" rel="stylesheet">

  <!-- Custom fonts for this template -->
  <link href="vendor/fontawesome-free/css/all.min.css" rel="stylesheet" type="text/css">
  <!-- <link href='css/lora.css' rel='stylesheet' type='text/css'> -->
  <!-- <link href='css/open-sans.css' rel='stylesheet' type='text/css'> -->

  <!-- Custom styles for this template -->
  <link href="css/clean-blog.min.css" rel="stylesheet">

</head>

<body>

  <!-- Navigation -->
  <nav class="navbar navbar-expand-lg navbar-light fixed-top" id="mainNav">
    <div class="container">
      <a class="navbar-brand" href="index.php">Demo Lab</a>
      <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
        Menu
        <i class="fas fa-bars"></i>
      </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <a class="nav-link" href="login.php"> Login </a>          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Page Header -->
  <header class="masthead" style="background-image: url('img/home-bg.jpg')">
    <div class="overlay"></div>
    <div class="container">
      <div class="row">
        <div class="col-lg-8 col-md-10 mx-auto">
          <div class="site-heading">
            
          </div>  
        </div>
      </div>
    </div>
  </header>

  <!-- Main Content -->
  <div class="container">
    <div class="row">
      <div class="col-lg-8 col-md-10 mx-auto">
        <div class="post-preview">
          <a href="post.php">
            <h2 class="post-title">
              CTF.LIVE 
            </h2>
            <h3 class="post-subtitle">
              Free for all public Capture the Flag Competition
            </h3>
          </a>
          <p class="post-meta">Posted by
            <a href="#">Attack Defense</a>
            on March 29, 2020</p>
        </div>
        <hr>
        <div class="post-preview">
          <a href="post.php">
            <h2 class="post-title">
              Attack Defense Lab Overview. 
            </h2>
            <h3 class="post-subtitle">
              Cybersecurity Education Platform at affordable price.
            </h3>
          </a>
          <p class="post-meta">Posted by
            <a href="#">Attack Defense</a>
            on March 16, 2019</p>
        </div>
       
      </div>
    </div>
  </div>

  <hr>

  <!-- Footer -->
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-lg-8 col-md-10 mx-auto">
          <ul class="list-inline text-center">
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fas fa-circle fa-stack-2x"></i>
                  <i class="fab fa-twitter fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fas fa-circle fa-stack-2x"></i>
                  <i class="fab fa-facebook-f fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fas fa-circle fa-stack-2x"></i>
                  <i class="fab fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
          <p class="copyright text-muted">Copyright &copy; Your Website 2019</p>
        </div>
      </div>
    </div>
  </footer>

  <!-- Bootstrap core JavaScript -->
  <script src="vendor/jquery/jquery.min.js"></script>
  <script src="vendor/bootstrap/js/bootstrap.bundle.min.js"></script>

  <!-- Custom scripts for this template -->
  <script src="js/clean-blog.min.js"></script>

</body>

</html>


┌──(root㉿INE)-[~]
└─# curl -v http://192.190.82.3                                                                                                                                                            
*   Trying 192.190.82.3:80...
* Connected to 192.190.82.3 (192.190.82.3) port 80
> GET / HTTP/1.1
> Host: 192.190.82.3
> User-Agent: curl/8.8.0
> Accept: */*
> 
* Request completely sent off
< HTTP/1.1 200 OK
< Date: Mon, 29 Sep 2025 14:11:34 GMT
< Server: Apache
< X-Powered-By: PHP/5.5.9-1ubuntu4.25
< Set-Cookie: PHPSESSID=pe29nbl8qiv2kg2keg0g9cbec2; path=/
< Expires: Thu, 19 Nov 1981 08:52:00 GMT
< Cache-Control: no-store, no-cache, must-revalidate, post-check=0, pre-check=0
< Pragma: no-cache
< Vary: Accept-Encoding
< Content-Length: 4408
< Content-Type: text/html
< 

<!DOCTYPE html>
<html lang="en">

<head>

  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <meta name="description" content="">
  <meta name="author" content="">

  <title>Attack Defense Demo Blog</title>

  <!-- Bootstrap core CSS -->
  <link href="vendor/bootstrap/css/bootstrap.min.css" rel="stylesheet">

  <!-- Custom fonts for this template -->
  <link href="vendor/fontawesome-free/css/all.min.css" rel="stylesheet" type="text/css">
  <!-- <link href='css/lora.css' rel='stylesheet' type='text/css'> -->
  <!-- <link href='css/open-sans.css' rel='stylesheet' type='text/css'> -->

  <!-- Custom styles for this template -->
  <link href="css/clean-blog.min.css" rel="stylesheet">

</head>

<body>

  <!-- Navigation -->
  <nav class="navbar navbar-expand-lg navbar-light fixed-top" id="mainNav">
    <div class="container">
      <a class="navbar-brand" href="index.php">Demo Lab</a>
      <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
        Menu
        <i class="fas fa-bars"></i>
      </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <a class="nav-link" href="login.php"> Login </a>          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Page Header -->
  <header class="masthead" style="background-image: url('img/home-bg.jpg')">
    <div class="overlay"></div>
    <div class="container">
      <div class="row">
        <div class="col-lg-8 col-md-10 mx-auto">
          <div class="site-heading">
            
          </div>  
        </div>
      </div>
    </div>
  </header>

  <!-- Main Content -->
  <div class="container">
    <div class="row">
      <div class="col-lg-8 col-md-10 mx-auto">
        <div class="post-preview">
          <a href="post.php">
            <h2 class="post-title">
              CTF.LIVE 
            </h2>
            <h3 class="post-subtitle">
              Free for all public Capture the Flag Competition
            </h3>
          </a>
          <p class="post-meta">Posted by
            <a href="#">Attack Defense</a>
            on March 29, 2020</p>
        </div>
        <hr>
        <div class="post-preview">
          <a href="post.php">
            <h2 class="post-title">
              Attack Defense Lab Overview. 
            </h2>
            <h3 class="post-subtitle">
              Cybersecurity Education Platform at affordable price.
            </h3>
          </a>
          <p class="post-meta">Posted by
            <a href="#">Attack Defense</a>
            on March 16, 2019</p>
        </div>
       
      </div>
    </div>
  </div>

  <hr>

  <!-- Footer -->
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-lg-8 col-md-10 mx-auto">
          <ul class="list-inline text-center">
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fas fa-circle fa-stack-2x"></i>
                  <i class="fab fa-twitter fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fas fa-circle fa-stack-2x"></i>
                  <i class="fab fa-facebook-f fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fas fa-circle fa-stack-2x"></i>
                  <i class="fab fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
          <p class="copyright text-muted">Copyright &copy; Your Website 2019</p>
        </div>
      </div>
    </div>
  </footer>

  <!-- Bootstrap core JavaScript -->
  <script src="vendor/jquery/jquery.min.js"></script>
  <script src="vendor/bootstrap/js/bootstrap.bundle.min.js"></script>

  <!-- Custom scripts for this template -->
  <script src="js/clean-blog.min.js"></script>

</body>

</html>

* Connection #0 to host 192.190.82.3 left intact

┌──(root㉿INE)-[~]
└─# curl -v -X POST http://192.190.82.3                                                                                                                                                    
*   Trying 192.190.82.3:80...
* Connected to 192.190.82.3 (192.190.82.3) port 80
> POST / HTTP/1.1
> Host: 192.190.82.3
> User-Agent: curl/8.8.0
> Accept: */*
> 
* Request completely sent off
< HTTP/1.1 405 Method Not Allowed
< Date: Mon, 29 Sep 2025 14:13:47 GMT
< Server: Apache
< X-Powered-By: PHP/5.5.9-1ubuntu4.25
< Set-Cookie: PHPSESSID=u83v9b6p3aeqooncosqudgklm5; path=/
< Expires: Thu, 19 Nov 1981 08:52:00 GMT
< Cache-Control: no-store, no-cache, must-revalidate, post-check=0, pre-check=0
< Pragma: no-cache
< Content-Length: 222
< Content-Type: text/html
< 
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>405 Method Not Allowed</title>
</head><body>
<h1>Method Not Allowed</h1>
<p>The requested method POST is not allowed for the URL /.</p>
</body></html>
* Connection #0 to host 192.190.82.3 left intact

┌──(root㉿INE)-[~]
└─# curl -v -X OPTIONS http://192.190.82.3                                                                                                                                           
*   Trying 192.190.82.3:80...
* Connected to 192.190.82.3 (192.190.82.3) port 80
> OPTIONS / HTTP/1.1
> Host: 192.190.82.3
> User-Agent: curl/8.8.0
> Accept: */*
> 
* Request completely sent off
< HTTP/1.1 200 OK
< Date: Mon, 29 Sep 2025 14:15:21 GMT
< Server: Apache
< X-Powered-By: PHP/5.5.9-1ubuntu4.25
< Set-Cookie: PHPSESSID=aej07ldi0v3j2lpg6ulgqgn922; path=/
< Expires: Thu, 19 Nov 1981 08:52:00 GMT
< Cache-Control: no-store, no-cache, must-revalidate, post-check=0, pre-check=0
< Pragma: no-cache
< Allow: GET,HEAD,OPTIONS
< Content-Length: 0
< Content-Type: text/html
< 
* Connection #0 to host 192.190.82.3 left intact

┌──(root㉿INE)-[~]
└─# curl -v -X HEAD http://192.190.82.3                                                                                                                                         
Warning: Setting custom HTTP method to HEAD with -X/--request may not work the 
Warning: way you want. Consider using -I/--head instead.
*   Trying 192.190.82.3:80...
* Connected to 192.190.82.3 (192.190.82.3) port 80
> HEAD / HTTP/1.1
> Host: 192.190.82.3
> User-Agent: curl/8.8.0
> Accept: */*
> 
* Request completely sent off
< HTTP/1.1 200 OK
< Date: Mon, 29 Sep 2025 14:18:40 GMT
< Server: Apache
< X-Powered-By: PHP/5.5.9-1ubuntu4.25
< Set-Cookie: PHPSESSID=nbiq3iplombsivjrp8q9mhhvk4; path=/
< Expires: Thu, 19 Nov 1981 08:52:00 GMT
< Cache-Control: no-store, no-cache, must-revalidate, post-check=0, pre-check=0
< Pragma: no-cache
< Content-Type: text/html
< 
* no chunk, no close, no size. Assume close to signal end

* Closing connection


Attaching  Basic HTTP Authentication


