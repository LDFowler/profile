<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8" />
    <!-- Required meta tags always come first -->
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />

    
    <!-- build:css css/main.css -->
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css" />
    <link rel="stylesheet" href="node_modules/font-awesome/css/font-awesome.min.css" />
    <link rel="stylesheet" href="node_modules/bootstrap-social/bootstrap-social.css" />
    <link rel="stylesheet" href="css/styles.css" />
    <!-- endbuild -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lobster|Open+Sans" />


    <title>NuCamp: A Better Way To Camp</title>
</head>

<body>
    <!--JUMBOTRON-->
    <header class="jumbotron jumbotron-fluid">
        <div class="container">
            <div class="row">
                <div class="col-4 col-sm-3 col-md-2 align-self-center">
                    <img src="img/logo.png" class="img-fluid" />
                 </div>
                <div class="col">
                    <h1>NuCamp</h1>
                    <h2>a better way to camp</h2>
                </div>
                <div class="col-md-4 col-xl-2 mt-4">
                    <a role="button" class="btn btn-lg btn-info" id="reserveButton">Reserve Campsite</a>
                </div>
            </div>
        </div>
    </header>
    
    <!--NAVBAR-->
  
    <nav class="navbar navbar-expand-sm navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#"><img src="img/logo.png" height="30" width="30" /></a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#nucampNavbar">...</button>
            <div class="collapse navbar-collapse" id="nucampNavbar">
                <ul class="navbar-nav">
                    <li class="nav-item active"><a class="nav-link" href="#"><i class="fa fa-home fa-lg"></i> Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="aboutus.html"><i class="fa fa-info fa-lg"></i> About</a></li>
                    <li class="nav-item"><a class="nav-link" href="#"><i class="fa fa-list fa-lg"></i> Sites</a></li>
                    <li class="nav-item"><a class="nav-link" href="contactus.html"><i class="fa fa-address-card fa-lg"></i> Contact</a></li>
                </ul>
                <span class="navbar-text ml-auto">
                    <a role="button" id="loginButton">
                        <i class="fa fa-sign-in"></i> Login
                    </a>
                </span>
            </div>
        </div>
    </nav>
    
    <!--RESERVE FORM-->
    <div id="reserveModal" class="modal fade" role="dialog">
        <div class="modal-dialog modal-lg" role="document">
            <div class="modal-content">
                <div class="modal-header ">
                    <h3 class="modal-title">Reserve a Campsite</h3>
                    <button type="button" class="close" data-dismiss="modal"> &times;</button>
                </div>
                <div class="modal-body">
                    <div class="container-fluid">
                        <form>
                            <div class="row form-group">
                                <div class="col-sm-6 col-form-label">   
                                    <label for="Number of Campers" text="Number of Campers" name="Number of Campers" id="numCampers">Number of Campers
                                        <select class="form-control" >
                                            <option>Select</option>
                                            <option>1</option>
                                            <option>2</option>
                                            <option>3</option>
                                            <option>4</option>
                                            <option>5</option>
                                            <option>6</option>
                                        </select>
                                    </label>
                                </div>
                            </div>
                            <div class="row form-group">
                                <div class="col-sm-6 col-form-label">
                                    <label class=""  for="date">Date</label><br />
                                        <input type="date" id="Date" name="Date"  placeholder="MM/DD/YYYY">
                                    </label>  
                                </div>
                            </div> 
                            
                            <!--Tent or RV-->
                            <div class="row form-group">
                                <div class="btn-group btn-group-toggle" data-toggle="buttons">
                                    <label class="btn btn-success active">
                                        <input type="radio" name="siteType" id="siteTent" autocomplete="off">Tent
                                    </label>
                                    <label class="btn btn-primary">
                                    <input type="radio" name="siteType" id="siteTent" autocomplete="off">RV
                                    </label>  
                                </div>
                            </div>     
                                
                            
                            <div class="row form-group">
                               <div class="col col-form-label" text="Search">
                                    <button type="submit" class="btn btn-secondary btn-sm ml-auto" data-dismiss="modal">Cancel</button>
                                    <button type="submit" class="btn btn-primary btn-sm ml-1">Search</button>
                                </div> 
                             </div>      
                         </form>
                     </div>
                 </div>
             </div>
         </div>
     </div>
          
    

                         
    
    <!--lOGIN MODAL-->
    <div id="loginModal" class="modal fade" role="dialog">
        <div class="modal-dialog " role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h3 class="modal-title">Login</h3>
                    <button type="button" class="close" data-dismiss="modal">&times;</button>
                </div>
                <div class="modal-body">
                    <div class="container-fluid">
                        <form>
                            <div class="form-row">
                                <div class="form-group col-12">
                                    <label class="sr-only" for="loginEmail">Email address</label>
                                    <input type="email" class="form-control form-control-sm" id="loginEmail" placeholder="Enter email">
                                </div>
                                <div class="form-group col-12">
                                    <label class="sr-only" for="loginPassword">Password</label>
                                    <input type="password" class="form-control form-control-sm" id="loginPassword" placeholder="Password">
                                </div>
                                <div class="col">
                                    <div class="form-check">
                                        <input class="form-check-input" type="checkbox">
                                        <label class="form-check-label"> Remember me</label>
                                    </div>
                                </div>
                            </div>
                            <div class="form-row">
                                <button type="button" class="btn btn-secondary btn-sm ml-auto" data-dismiss="modal">Cancel</button>
                                <button type="submit" class="btn btn-primary btn-sm ml-1">Sign in</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>


    <div class="container">
    <!--carousel-->      
        <div class="row row-content">
            <div class="col-md-8 mx-auto">
                <div id="homeCarousel" class="carousel slide" data-ride="carousel">
                    <ol class="carousel-indicators">
                        <li data-target="#homeCarousel" data-slide-to="0" class="active"></li>
                        <li data-target="#homeCarousel" data-slide-to="1"></li>
                        <li data-target="#homeCarousel" data-slide-to="2"></li>
                    </ol>
                    <div class="carousel-inner">
                        <div class="carousel-item active">
                            <img class="d-block w-100" src="img/breadcrumb-trail.jpg" alt="Breadcrumb Trail Campground" />
                            <div class="carousel-caption">
                                <h3>Breadcrumb Trail Campground</h3>
                                <p class="d-none d-sm-block">Let Nucamp be your guide to this off-the-beaten-path, hike-in-only campground.</p>
                            </div>
                        </div>
                        <div class="carousel-item">
                            <img class="d-block w-100" src="img/react-lake.jpg" alt="React Lake Campground" />
                            <div class="carousel-caption">
                                <h3>React Lake Campground</h3>
                                <p class="d-none d-sm-block">Nestled in the foothills of the Chrome Mointains this campground on the shores of the pristine 
                                    React Lake is a favorite for fly fishers.</p>
                            </div>
                        </div>
                        <div class="carousel-item">
                            <img class="d-block w-100" src="img/chrome-river.jpg" alt="Chrome River Campground" />
                            <div class="carousel-caption">
                                <h3>Chrome River Campground</h3>
                                <p class="d-none d-sm-block">Spend a few sunny days and starry nights beneath a canopy of old-growth firs at this enchanting spot by the Chrome River"></p>
                            </div>
                        </div>
                    </div>
                    <a class="carousel-control-prev" href="#homeCarousel" role="button" data-slide="prev">
                        <span class="carousel-control-prev-icon"></span>
                        <span class="sr-only">Previous</span>
                    </a>
                    <a class="carousel-control-next" href="#homeCarousel" role="button" data-slide="next">
                        <span class="carousel-control-next-icon"></span>
                        <span class="sr-only">Next</span>
                    </a>
                    <div class="btn-group" id="carouselButton">
                        <button class="btn btn-danger btn-sm" id="carouselButton">
                            <i class="fa fa-pause"></i>
                        </button>
                    </div>
                </div>
            </div><!--/.MX-AUTO-->
        </div><!--/.ROW-->
                       
                      
                       
                    
        <!--Discover and Review-->                    
        <div class="row row-content align-items-center">
            <div class="col-sm-4 order-sm-last col-md-3">
                <h2 class="text-sm-right">Discover & Review</h2>
            </div> 
            <div class="col">
                <div class="media">
                    <img class="d-flex mr-3 img-thumbnail" src="img/breadcrumb-trail-thumb.jpg" alt="Breadcrumb Trail" />
                    <div class="media-body align-self-center"
                        <h3>Our Campsites</h3>
                        <p class="d-none d-sm-block">Explore our growing database of curated campsites and leave your own reviews!</p>
                    </div>
                </div>
            </div>
        </div>
                
               
        <div class="row row-content align-items-center">
            <div class="col-sm-4 order-sm- col-md-3">
                <h2 class="text-sm-right">Featured Campsites</h2>
            </div> 
            <div class="col">
                <div class="media">
                   <div class="media-body align-self-center">
                        <h3>React Lake Campground</h3>
                        <p class="d-none d-sm-block">Nestled in the foothills of the Chrome Mountains, this campground on the shores of the pristine React Lake is a favorite for fly fishers.</p>
                    </div>
                    <img class="d-flex ml-3 img-thumbnail" src="img\react-lake-thumb.jpg" alt="React-Lake" />
                </div>
            </div>   
        </div>
    
    
        <div class="row row-content align-items-center">
            <div class="col-sm4 order-sm-last col-md-3">
                <h2 class="text-sm-right">Our Community Partners</h2>
            </div>
            <div class="col">
                <div class="media">
                    <img class="d-flex mr-3 img-thumbnail" src="img/bootstrap-thumb.png" alt="Bootstrap Outfitters" />
                    <div class="media-body align-self-center">
                        <h3>Bootstrap Outfitters</h3>
                        <p class="d-none d-sm-block">Bootstrap Outfitters supplies you with gear you need at prices you can't beat.</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="row row-content">
            <div class="col-sm-6 mx-auto">
                <div class="card">
                    <h3 class="card-header bg-info text-white">Reserve a Campsite</h3>
                    <div class="card-body">
                       <form id="reserveForm">
                            <div class="row form-group">
                                <div class="col-sm-6 col-form-label">   
                                    <label for="Number of Campers" text="Number of Campers" name="Number of Campers" id="numCampers">Number of Campers
                                        <select class="form-control" >
                                            <option>Select</option>
                                            <option>1</option>
                                            <option>2</option>
                                            <option>3</option>
                                            <option>4</option>
                                            <option>5</option>
                                            <option>6</option>
                                        </select>
                                    </label>
                                </div>
                            </div>
                            <div class="row form-group">
                                <div class="col-sm-6 col-form-label">
                                    <label for="date">Date</label><br />
                                        <input type="date" id="Date" name="Date"  placeholder="MM/DD/YYYY">
                                    </label>  
                                </div>
                            </div>     
                            
                            <div class="row form-group">
                               <div class="col col-form-label" text="search">
                                <button type="button" class="btn btn-primary">Search
                                   
                                </button>
                               </div> 
                            </div>        
                        </form> 
                    </div>
                </div>
            </div>
        </div>           
    </div>
                            
    
    <!--FOOTER SECTION-->
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-4 col-sm-2 offset-1">
                    <h5>Links</h5>
                    <ul class="list-unstyled">
                        <li><a href="#">Home</a></li> 
                       <li><a href="aboutus.html">About</a></li> 
                       <li><a href="#">Sites</a></li> 
                       <li><a href="contactus.html">Contact</a></li> 
                    </ul>
                </div>
        
                <div class="col-6 col-sm-5 text-center">
                    <h5>Social</h5>
                    <a class="btn btn-social-icon btn-instagram" href="http://instagram.com/"><i class="fa fa-instagram"></i></a>
                    <a class="btn btn-social-icon btn-facebook" href="http://facebook.com/"><i class="fa fa-facebook"></i></a>
                    <a class="btn btn-social-icon btn-twitter" href="http://twitter.com/"><i class="fa fa-twitter"></i></a>
                    <a class="btn btn-social-icon btn-google" href="http://youtube.com/"><i class="fa fa-youtube"></i></a>
                </div>
                
                <div class="col-sm-4 text-center">
                    <a role="button" class="btn btn-link" href="tel:+12065551234"><i class="fa fa-phone"></i> 1-206-555-1234</a><br />
                    <a role="button" class="btn btn-link" href="mailto:campsites@nucamp.co"><i class="fa fa-envelope-o"></i> campsites@nucamp.co</a>
                </div>
            </div> 
        </div>
    </footer>
    
    
       <!-- build:js js/main.js -->
       <script src="node_modules/jquery/dist/jquery.slim.min.js"></script>
       <script src="node_modules/popper.js/dist/umd/popper.min.js"></script>
       <script src="node_modules/bootstrap/dist/js/bootstrap.min.js"></script>
       <script src="js/scripts.js"></script>
       <!-- endbuild -->
    

    <script> 
        $(function() {
            $(".carousel").carousel({
                interval: 2000                               
            })
            $("#carouselButton").click(function() {
                $(".carousel").carousel("pause");
                if($("#carouselButton").children("i").hasClass("fa-pause")) {
                    $(".carousel").carousel("pause");
                    $("#carouselButton").children("i").removeClass("fa-pause");
                    $("#carouselButton").children("i").addClass("fa-play")
                } else {
                    $(".carousel").carousel("cycle");
                    $(".carouselButton").children("i").removeClass("fa-play");
                    $(".carouselButton").children("i").addClass("fa-pause");
                }
            });
        });
    </script>       


</body>

</html>
