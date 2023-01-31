---
layout: sageLayout
title: Quadric Surfaces
show_in_menu: false
permalink: /Quadric
---
  <head>
    <script src="https://sagecell.sagemath.org/static/embedded_sagecell.js"></script>
    <script>
    // Make the div with id 'mycell' a Sage cell
    sagecell.makeSagecell({inputLocation:  '#mycell',
                           template:       sagecell.templates.minimal,
                           linked:         True,
                           evalButtonText: 'Activate'});
    // Make *any* div with class 'compute' a Sage cell
    sagecell.makeSagecell({inputLocation: 'div.compute',
                           evalButtonText: 'Evaluate'});
    </script>
  </head>
  <div class="container-fluid">
  <h1>Examples of cylinders and quadric surfaces</h1>
  <p>A description of quadric surfaces in three-space. Let's look at our first example, the sphere.</p>
  <h3>A sphere</h3>
    <div class="compute"><script type="text/x-sage">var('x','y','z');
implicit_plot3d(x^2+y^2+z^2==4, (x,-3,3), (y,-3,3), (z,-3,3))
      </script></div>

  <hr>

  <h3>Hyperboloid of one sheet</h3>
   <div class="compute"><script type="text/x-sage">var('x','y','z');
implicit_plot3d(x^2+y^2-z^2==4, (x,-5,5), (y,-5,5), (z,-3,3))
      </script></div>

  <hr>

  <h3>Hyperboloid of two sheets</h3>
     <div class="compute"><script type="text/x-sage">var('x','y','z');
implicit_plot3d(-x^2-y^2+z^2==4, (x,-5,5), (y,-5,5), (z,-6,6))
      </script></div>

  <hr>    

  <h3>Ellipsoid</h3>
     <div class="compute"><script type="text/x-sage">var('x','y','z');
implicit_plot3d(x^2+4*y^2+z^2==4, (x,-3,3), (y,-3,3), (z,-4,4))
      </script></div>

  <hr>

   <h3>Paraboloid</h3>
     <div class="compute"><script type="text/x-sage">var('x','y','z');
implicit_plot3d(2*x^2 + z^2==y, (x,-3,3), (y,-3,3), (z,-4,4))
      </script></div>

  <hr>

  <h3>A saddle surface</h3>
     <div class="compute"><script type="text/x-sage">var('x','y','z');
implicit_plot3d(x^2 - z^2==y, (x,-3,3), (y,-3,3), (z,-4,4))
      </script></div>

  <hr>

   <h3>A more interesting surface</h3>
    <div class="compute"><script type="text/x-sage">var('x','y','z');
T = RDF(golden_ratio);
F = 2 - (cos(x+T*y) + cos(x-T*y) + cos(y+T*z) + cos(y-T*z) + cos(z-T*x) + cos(z + T*x))
r = 4.77
implicit_plot3d(F, (x,-r,r), (y,-r,r), (z,-r,r), plot_points=100)
      </script></div>
</div>