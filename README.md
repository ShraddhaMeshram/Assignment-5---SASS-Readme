# Assignment-5---SASS-Readme

# Assignment-5---SASS
 My painting Website

 ## Feature Used

 1)for responsive banner section used css grid.
 2)for responsive category section used css grid.
 3)for responsive products section used css grid.
 4)for responsive about section used css flexbox.
 5)for responsive gallery section used css grid.
 6)for responsive review card section used css grid.
 7)for responsive blogs section used css grid.
 8)for responsive contact form section used css grid and flexbox.
 9)for responsive footer section used css grid.

 Variables-to store value color and fonts
$green:#4294b9;
$black:#222;
$white:#fff;
$light-color:#666;
$light-bg:#f3f3f3;
$border:.1rem solid rgba(0,0,0,.1);
$box-shadow:0 .5rem 1rem rgba(0,0,0,.1);


 nesting-nesting child selector inside parent
.box{
      display: flex;
      align-items: center;
      gap:1.5rem;
      margin-bottom: 1.5rem;
      position: relative;

      .fa-times{
        position: absolute;
        top:50%; right:2rem;
        transform: translateY(-50%);
        font-size: 2rem;
        color:$light-color;
        cursor: pointer;

        &:hover{
          color:$green;
        }
      }
---------------------------------------------------
.heading {
  h1 {
    color: #222;
  }
  p {
    font-size: 2rem;
    color: #666;
  }
}
---------------------------------------------------
 mixin-We use them to group together multiple CSS declarations for reuse throughout our projects
 @mixin grid($val) {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax($val, 1fr));
  gap:1.5rem;
}
---------------------------------------------------
@mixin button-styles {
  background: #4294b9;
  color: #fff;
}

.btn {
  @include button-styles;
}
---------------------------------------------------

Interpolation: You've used interpolation to generate property names. For instance, you dynamically generate property names using interpolation within the .heading rule:

$text-property: 'color';
.heading {
  #{$text-property}: #222;
}
---------------------------------------------------
