This fork illustrates how to implement an extension of 2-way Factorization Machines to (approximately) model interactions of order d (ideally 1 < d < 3) as per the paper [An Elementary View on Factorization Machines](https://dl.acm.org/citation.cfm?id=3109892).

This is supported only for training with (vanilla) SGD. To use, just pass the desired order to the option -order, which by default is equal to 2.0.

Please note that this implementation serves illustrative purposes only. It contains the minimal number of modifications needed to get the variant running, but is slow due to the use of the pow function. You can tailor the code to your needs and use the sqrt function instead for some specific values of d, such as d = 1.25, 1.5, 1.75 and so on, which greatly speeds up the computations.

libFM
=====

Library for factorization machines

web: http://www.libfm.org/

forum: https://groups.google.com/forum/#!forum/libfm

Factorization machines (FM) are a generic approach that allows to mimic most factorization models by feature engineering. This way, factorization machines combine the generality of feature engineering with the superiority of factorization models in estimating interactions between categorical variables of large domain. libFM is a software implementation for factorization machines that features stochastic gradient descent (SGD) and alternating least squares (ALS) optimization as well as Bayesian inference using Markov Chain Monte Carlo (MCMC).

Compile
=======
libFM has been tested with the GNU compiler collection and GNU make. libFM and the tools can be compiled with
> make all

Usage
=====
Please see the [libFM 1.4.2 manual](http://www.libfm.org/libfm-1.42.manual.pdf) for details about how to use libFM. If you have questions, please visit the [forum](https://groups.google.com/forum/#!forum/libfm).
