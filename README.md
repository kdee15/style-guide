Project Style Guide
===========

Below is a brief style guide that is useful when working on multi-person teams in the front end environment.

## File Structure Guidelines

Keep file structures in a consistent pattern for each project, allows all of us to just dive into a project and work. This is the current suggested pattern:

* PROJECT ROOT
    * index.html
    * humans.txt
    * robots.txt
    * etc...
    * assets/
        * js/
            * libraries/
            * scripts/
            * production.js
            * production.min.js
        * Images/
            * site/
            * posts/
            * products/
        * css/
            * Stylesheet.css
            * etc...

- - -

## Commenting Guidelines

Commenting code in a consistent and uniform manner is vital to working as a team. It allows everyone to expect a certain pattern, meaning they can navigate and find certain items quickly.

Following the pattern is half the battle. Useful, descriptive comments make up the other half. We need to know exactly what each section / component does, and whether there are any things we need to take note of.

Sectioning of segments of code makes it easy to read through code in a predictable manner. Always opt for more comments. We can always strip them out with Grunt.js on production sites. 

### HTML

    <body>
        <!--[if lt IE 7]>
            <p class="chromeframe">You are using an <strong>outdated</strong> browser. Please <a href="http://browsehappy.com/">upgrade your browser</a> or <a href="http://www.google.com/chromeframe/?redirect=true">activate Google Chrome Frame</a> to improve your experience.</p>
        <![endif]-->
    	
    	<!-- C. WORK AREA ++++++++++++++++++++++++++++++++++++++ -->
    	
    		<!-- C.1. MASTHEAD -->
    		
    		<header id="masthead">
    		
    		    <!-- C.1.1. Logo -->
    		    <img src="" class="logo" alt="" />
    		    
    		    <!-- C.1.2. Main Navigation
    		    <nav class="main navigation">
    		    
    		        <ul>
    		            <li><a href="#">Link Text</a></li>
    		            <li><a href="#">Link Text</a></li>
    		            <li><a href="#">Link Text</a></li>
    		            <li><a href="#">Link Text</a></li>
    		        </ul>
    		    
    		    </nav>
    		
    		</header>
    		
    		<!-- C.1. END -->
    	
    	<!-- C. END ++++++++++++++++++++++++++++++++++++++ -->
    	
        <!-- D. JAVASCRIPT ++++++++++++++++++++++++++++++++++++++ -->
        
        	<!-- D.1. JQUERY -->
            <script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
            <script>window.jQuery || document.write('<script src="assets/js/vendor/jquery-1.9.1.min.js"><\/script>')</script>
    		
    		<!-- D.2. SITE -->
            
            <!-- D.3. GOOGLE ANALYTICS -->
            <script>
                var _gaq=[['_setAccount','UA-XXXXX-X'],['_trackPageview']];
                (function(d,t){var g=d.createElement(t),s=d.getElementsByTagName(t)[0];
                g.src=('https:'==location.protocol?'//ssl':'//www')+'.google-analytics.com/ga.js';
                s.parentNode.insertBefore(g,s)}(document,'script'));
            </script>
            
        <!-- D. END ++++++++++++++++++++++++++++++++++++++ -->
        
    </body>

### Javascript

    // 1. REVEAL SCRIPT ++++++++++++++++++++++++++++++++++++
    
    jQuery(document).ready(function($) {
    $(".reveal").click(function(e) {
        var target = $(this).attr('href');
        if ($(target).css('display') === 'none') {
          $(target).fadeIn(130);
        }
        else {
          $(target).fadeOut(130);
        }
        e.preventDefault();
      });
    });
    
    // 1. END ++++++++++++++++++++++++++++++++++++

### CSS

We use SCSS (SASS) as our CSS pre-processor, therefore we implement comments using the SASS comment format. This will strip out the comments on processing, giving us a cleaner output CSS.

    // A. BIG SECTION LIKE A PAGE OR A FEATURE (ex: MAST) ++++++++++++++++++++++++++++++++++++
    
        #masthead {
    
        // A.1. MAJOR COMPONENT WITHING SECTION (ex: SIDEBAR)
        
            .sidebar {
            
                // A.1.1. Minor component
                
                // NOTE: This block is overridden from the default reusable pattern at [B.1.1. Generic Block]. 
                
                .aside-block {}
                
                // A.1.1. End
            
            }
        
        // A.1. END
        
        }
    
    // A. END ++++++++++++++++++++++++++++++++++++

- - -
