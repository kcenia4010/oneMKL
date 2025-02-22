.. SPDX-FileCopyrightText: 2019-2020 Intel Corporation
..
.. SPDX-License-Identifier: CC-BY-4.0

.. _onemkl_lapack_gerqf_scratchpad_size:

gerqf_scratchpad_size
=====================

Computes size of scratchpad memory required for :ref:`onemkl_lapack_gerqf` function.

.. container:: section

  .. rubric:: Description
         
``gerqf_scratchpad_size`` supports the following precisions.

     .. list-table:: 
        :header-rows: 1
  
        * -  T 
        * -  ``float`` 
        * -  ``double`` 
        * -  ``std::complex<float>`` 
        * -  ``std::complex<double>`` 

Computes the number of elements of type ``T`` the scratchpad memory to be passed to :ref:`onemkl_lapack_gerqf` function should be able to hold.
Calls to this routine must specify the template parameter
explicitly.

gerqf_scratchpad_size
---------------------

.. container:: section

  .. rubric:: Syntax

.. code-block:: cpp

    namespace oneapi::mkl::lapack {
      template <typename T>
      std::int64_t gerqf_scratchpad_size(cl::sycl::queue &queue, std::int64_t m, std::int64_t n, std::int64_t lda)
    }

.. container:: section

  .. rubric:: Input Parameters
         
queue
   Device queue where calculations by the gerqf (buffer or USM version) function will be performed.

m
   The number of rows in the matrix :math:`A` (:math:`0 \le m`).

n
   The number of columns in the matrix :math:`A` (:math:`0 \le n`).

lda
   The leading dimension of ``a``; at least :math:`\max(1,m)`.

.. container:: section

  .. rubric:: Return Value

The number of elements of type ``T`` the scratchpad memory to be passed to :ref:`onemkl_lapack_gerqf` function should be able to hold.

**Parent topic:** :ref:`onemkl_lapack-linear-equation-routines`

