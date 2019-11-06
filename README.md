# sudoku
scripts for checking and generating images of sudokus

Takes two 81-character strings, one sudoku problem (with dots representing blanks) and one solution. Example:

```
$ sudoku 6..8.32.......9.41.9..2........173...1.9.8.7...863........9..5.92.3.......37.6..4 641873295832569741597421638459217386316948572278635419764192853925384167183756924
```

| `problem.png` | `solution.png` |
| ------- | -------- |
| ![alt text](https://github.com/benzlock/sudoku/blob/master/ex-problem.png "example problem" ) | ![alt text](https://github.com/benzlock/sudoku/blob/master/ex-solution.png "example solution" ) |

* If it receives both a problem and a solution, both files will be produced, with additional formatting in `solution.png` to show what is not included in the problem.
  If only a problem (a string that contains one or more dots) is received, only `problem.png` will be produced; if only a solution (a string that contains no dots) is received,
  only `solution.png` will be produced, but it will not have the special formatting.
* The `-pf`, `-sf`, and `-f` options can be used to specify the problem formatting, solution formatting, and font in LaTeX style.
  By default, `-pf` is `\Huge{`, `-sf` is `\textcolor{red}{\Huge{`, and `-f` is `cmbright`.
* The validity of the solution is checked, as well as and whether the problem and solution match, or `problem[i] = solution[i]` if `problem[i]` is not a dot.

Requires `pdflatex` and [ImageMagick](https://imagemagick.org/) to run.

