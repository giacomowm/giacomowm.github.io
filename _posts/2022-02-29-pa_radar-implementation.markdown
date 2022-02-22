
# Method



Suppose our radar depicts \\( n\\) values, \\( v_1,v_2, \ldots , v_n \in [0,1],\\) on \\( n\\) spokes of a radar chart. Consider two values \\( v_i, v_j \\) on adjacent spokes of our radar chart. In order to choose a curve we first define a curve in Cartesian coordinates, which we will transform later. There are many viable candidates curves but, for the sake of control and, importantly, so that we can find explicit solutions, we use the quadratic function \\( f ( x ) = a ( -\sqrt{v_i} ( 1-x ) +\sqrt{v_j}x ) ^{2} +( 1-a ) ( 1- ( -\sqrt{1-v_i} ( 1-x ) +\sqrt{1-v_j}x ) ^{2} ) \\) defined on the interval \\( [0,1]\\) joining the points \\( (0,v_i)\\) and \\( (1,v_j)\\). The function \\( f\\) depends on these values and a further parameter \\( a\\). The parameter \\( a\\) allows us adjust the area under the curve. The reason for choosing this function is that it has some desirable properties. Firstly, it is identically zero when \\( v_i = v_j = 0\\). Secondly, for \\( a \in [0,1]\\), the curve is bounded above by \\( 1\\) and below by \\( 0\\), and achieves these values for \\( a =0\\) and \\( a =1\\), respectively, and its stationary point always lies in the interval of definition.



Defining \\( g(\theta) = f(\frac{n \theta}{2 \pi}) + c\\) for some constant \\( c\\) creates a central counter on the hub of the plot when this function is plotted in polar coordinates \\( (r,\theta)\\), such that the values \\( v_i\\) and \\( v_j\\) lie on two adjacent spokes (an angle of \\( 2 \frac{pi}{n}\\) apart).<br>We can then solvefootnote{I recommend using a computer! I originally solved this in Maple but rewrote it for python using the texttt{sympi} package. Originally I used the function \\( f(x) = ( x-{\frac{1}{2}}+ ( a+1 ) ( v_j-v_i ) ) ( x-{\frac{1}{2}}- ( a-1) ( v_j-v_i) ) \\), which results in simpler solutions, but the shapes were not as well behaved.<br>



 for our parameter \\)a\\) such that the area enclosed between the line and counter is proportional to the average of the values, i.e.<br>\\( int_0^{frac{2pi}{n}} frac{1}{2} left(g(theta) right) ^2 , d theta - frac{pi c^2}{n} =frac{v_i+v_j}{2}p \\)<br>where \\)p\\) is the constant of proportionality.



We can then plot \\)g(theta)\\) in polar coordinates and fill the area under the curve. Doing this in each sector between each pair of adjacent values produces what we will term textit{the proportional area radar chart}, shown in various guises in cref{paradar}.<br><br>caption{Equal Area Radar Charts: four representations of the same data on a scale of \\)0\\) to \\)1\\): each radar chart represents four points of value \\)0.1\\), and four points of value \\)1\\).}label{paradar}<br>end{figure}%<br>Here we have used a counter offset of \\)c =1/2\\) and a constant of proportionality of \\)4\\).<br>Any constant of proportionality \\)p&gt;0\\) can be chosen; the resulting charts will be more 'bulbous' for larger \\)p\\)% (see cref{proportions})<br>.<br>Note that, in general, because the function \\)f\\) in cref{quad_func} is identically zero when \\)v_i,v_j =0\\), two adjacent zeroes are always connected by an arc of the circle with radius \\)r= c\\) and so no area is enclosed outside of the hub.



subsection*{Interpretability and Aestetics}<br>A comparison of the four radars in cref{bad_charts_better} and cref{paradar} shows that the area adjustment achieves visually what it does mathematically. Reordering has no effect on the area enclosed.<br>The substitutions made in the conversion to polar coordinates and the range of the integral in cref{polarsolver} over which we solve for \\)a\\) ensures that for any given \\)v_i,v_j\\) , the value of \\)a\\), and therefore the equation of the curve, is independent of the number of categories \\)n\\). There is a different effect on the shape, though, depending on the number of variables.<br>%Compare the charts in cref{various_numbers_of_categories}.<br>A possible future adjustment is to have the proportion, \\)p\\), vary with the number of categories, \\)n\\). For now, it suffices to select a suitable \\)p\\) once \\)n\\) is fixed.<br><br>The constant of proportionality \\)p\\) can be chosen so as not to make the shapes too extreme, and the presence of a sizeable central counter (\\)c=1/2\\) is used here) helps to reduce the differences in shapes.<br>Another effect of the use of different curves for higher or lower values is the different shapes produced.<br>Curves connecting small values bulge out a little near the hub, whereas curves connecting high values dip in, creating a spiky effect.<br>This means that higher and lower values are associated with different curves and so in addition to the overall shape profile of a radar being recognisable, even the shape profile of different values should be, given that the viewer has some experience in a consistent format.



If we use this visualisation for comparing football players, to take an example, an xT/xG profile of a player Inter signed following the 2017/18 season, Alexis Sanchez, and a player they did not, say Saido Berahino, one looks like a star, and the other doesn't---see cref{star} (for other examples see also cref{attack,defence,naga}).<br>The presence of a central counter allows for design elements to be placed in the center.<br>In this example we have the player's names centrally.<br>begin{figure}[tbp]centering<br>includegraphics[width=columnwidth]{star.png}<br>caption{A player comparison proportional area radar chart.}label{star}<br>end{figure}



PIC



All the charts in this article were created with a scipt I wrote. It is available to use along with instructions here: https://github.com/giacomowm/pa_radar
