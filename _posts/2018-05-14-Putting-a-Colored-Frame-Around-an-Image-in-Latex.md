---
layout: post
title: Putting a Colored Frame Around an Image in Latex
---

Sometimes it is nice to put a colored frame around an image in your Latex document. The ordinary frame command does not support coloring frames but we can use to two packages to achieve xcolor and adjustbox.
    
    \usepackage[HTML]{xcolor}
    \usepackage[export]{adjustbox}

The xcolor package allows us to use the HMTL Hex encoding of colors which is very convenient. However, it seems you need to define the color name to use it in for the image, like this, 

    \definecolor{my_magenta}{HTML}{FF00FF}

To put a frame around an image we just add some parameters to the `includegraphics` command,

    \includegraphics[cfbox=my_magenta 0.5pt 0pt]{my_image}

Where the parameters are `(color_name, border_width, inner_padding)` where the `inner_padding` parameter is a white colored border inside the box border. There are many more parameters to explore, e.g. background, etc. 

