### Solve the following problrem by using **trust-constr** method and **COBYLA** method:
$$\begin{array}{lll}
        \min_{x_1,x_2} & f(x_1,x_2)=-x_1-x_2 \\
        \mbox{s.t. } & -2x_1^4 + 8x_1^3 -8x_1^2 + x_2 - 2 \le 0  \\
         & -4x_1^4 + 32x_1^3 - 88x_1^2 + 96x_1 + x_2 -36 \le 0   \\
         & 0 \le x_1 \le 3 \\
         & 0 \le x_2 \le 4 \\
\end{array}$$

### Properties:
| **trust-constr**                                                                                            | **COBYLA**                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| can handle bounds on the variables in scipy                                                                 | cannot handle bounds on the variables in scipy                                                                        |
| can handle equality constraints in scipy                                                                    | cannot handle equality constraints in scipy                                                                           |
| trust region radius reduced when the approximations fail to yield an improvement                            | trust region radius reduced when the approximations fail to yield an improvement                                      |
| suitable for dealing with large-scale problems                                                              | easy to use for small numbers of variables                                                                            |
| trust region radius may increase                                                                            | trust region radius is never increased                                                                                |
| combines trust region strategies, interior point approaches and successive quadratic programming techniques | the main influence on the design was the belief that linear approximations to nonlinear constraints are highly useful |
| find a approximate solution to the barrier problem in each iteration                                        | form linear approximations to the objective and constraint functions  in each iteration                               |
| construct a quadratic model of the Lagrangian function in each iteration                                    | construct interpolation at the vertices of a simplex in each iteration                                                |
| information of first derivative and second derivative will be used                                          | information of first derivative and second derivative won't be used                                                   |
