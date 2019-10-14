# Prolog-Assignment

remaining : 

test cases for
  findpath
  
<h1> Instructions on Running and Testing the Code in this Project </h1>

<h2> Requirements </h2>

A working installation of <a href="https://www.swi-prolog.org/">SWI-Prolog</a> is needed to successfully execute the code in this project. 

<h2> Find Path </h2>

<pre>
?- find_path(a, b, Path, Sum).
Path = [a, b],
Sum = 5 ;
Path = [a, c, b],
Sum = 10 ;
Path = [a, c, d, b],
Sum = 261 ;
Path = [a, c, e, f, d, b],
Sum = 1509 ;
Path = [a, c, e, d, b],
Sum = 1212 ;
Path = [a, d, b],
Sum = 256 ;
Path = [a, d, e, c, b],
Sum = 966 ;
Path = [a, d, f, e, c, b],
Sum = 1263 ;
Path = [a, d, c, b],
Sum = 15 ;
Path = [a, g, f, e, d, b],
Sum = 403 ;
Path = [a, g, f, e, d, c, b],
Sum = 162 ;
Path = [a, g, f, e, c, b],
Sum = 1103 ;
Path = [a, g, f, e, c, d, b],
Sum = 1354 ;
Path = [a, g, f, d, b],
Sum = 598 ;
Path = [a, g, f, d, e, c, b],
Sum = 1308 ;
Path = [a, g, f, d, c, b],
Sum = 357 ;
false.
</pre>

<pre>
?- find_path(a, a, Path, Sum).
Path = [a],
Sum = 0 ;
false.
</pre>

<pre>
?- find_path(c, g, Path, Sum).
Path = [c, d, e, f, g],
Sum = 132 ;
Path = [c, d, f, g],
Sum = 327 ;
Path = [c, d, a, g],
Sum = 35 ;
Path = [c, d, b, a, g],
Sum = 286 ;
Path = [c, e, f, g],
Sum = 1073 ;
Path = [c, e, f, d, a, g],
Sum = 1283 ;
Path = [c, e, f, d, b, a, g],
Sum = 1534 ;
Path = [c, e, d, f, g],
Sum = 1278 ;
Path = [c, e, d, a, g],
Sum = 986 ;
Path = [c, e, d, b, a, g],
Sum = 1237 ;
Path = [c, b, d, e, f, g],
Sum = 383 ;
Path = [c, b, d, f, g],
Sum = 578 ;
Path = [c, b, d, a, g],
Sum = 286 ;
Path = [c, b, a, g],
Sum = 35 ;
Path = [c, b, a, d, e, f, g],
Sum = 142 ;
Path = [c, b, a, d, f, g],
Sum = 337 ;
Path = [c, a, g],
Sum = 30 ;
Path = [c, a, b, d, e, f, g],
Sum = 388 ;
Path = [c, a, b, d, f, g],
Sum = 583 ;
Path = [c, a, d, e, f, g],
Sum = 137 ;
Path = [c, a, d, f, g],
Sum = 332 ;
false.
</pre>


<h2> Sublist </h2>
<pre>
?- sublist([a, c], [a, b, c]).
false.
</pre>

<pre>
?- sublist([a], [a, b, c]).
true.
</pre>

<pre>
?- sublist([2, 3], [1, 2, 3, 4, 5]).
true.
</pre>

<h2> Has Triplicate </h2>
<pre>
?- has_triplicate([1, 1, 2, 3, 4, 1, 2, 3, 4, 5, 6, 2, 3]).
1
true ;
2
true ;
3
true ;
false.
</pre>

<pre>
?- has_triplicate([a, b, c, d, e, a, b, c, f, e, a, f]).
a
true ;
false.
</pre>

<pre>
?- has_triplicate([]).
false.
</pre>

<h2> Remove Nth </h2>
<pre>
?- remove_nth(3, [1, 2, 3, 4, 5, 6], Y).
Y = [1, 2, 4, 5, 6].
</pre>

<pre>
?- remove_nth(7, [1, 2, 3, 4], Y).
false.
</pre>

<pre>
?- remove_nth(7, [a, b, c, d, 1, 2, 3, 4], Y).
Y = [a, b, c, d, 1, 2, 4].
</pre>

<pre>
?- remove_nth(7, [], Y).
false.
</pre>

<h2> Remove Every Other </h2>

<pre>
?- remove_every_other([1, 2, 3, 4, 5, 6, 7], Y).
Y = [1, 3, 5, 7] .
</pre>

<pre>
?- remove_every_other([a, b, c, d, e, f], Y).
Y = [a, c, e].
</pre>

<pre>
?- remove_every_other([a], Y).
Y = [a]
</pre>

<pre>
?- remove_every_other([], Y).
Y = [].
</pre>
