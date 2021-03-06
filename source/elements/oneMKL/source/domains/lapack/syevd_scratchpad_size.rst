.. _onemkl_lapack_syevd_scratchpad_size:

syevd_scratchpad_size
=====================


.. container::


   Computes size of scratchpad memory required for :ref:`onemkl_lapack_syevd` function.


         ``syevd_scratchpad_size`` supports the following precisions.


         .. list-table:: 
            :header-rows: 1

            * -  T 
            * -  ``float`` 
            * -  ``double`` 




   .. container:: section


      .. rubric:: Description
         :class: sectiontitle


      Computes the number of elements of type T the scratchpad memory to be passed to :ref:`onemkl_lapack_syevd` function should be able to hold.
      Calls to this routine must specify the template parameter
      explicitly.


syevd_scratchpad_size
---------------------

.. container::

   .. container:: section


      .. rubric:: Syntax
         :class: sectiontitle


      .. container:: dlsyntaxpara


         .. cpp:function::  template <typename T>std::int64_t         onemkl::lapack::syevd_scratchpad_size(cl::sycl::queue &queue, onemkl::job jobz, onemkl::uplo upper_lower,         std::int64_t n, std::int64_t lda)

   .. container:: section


      .. rubric:: Input Parameters
         :class: sectiontitle


      queue
         Device queue where calculations by :ref:`onemkl_lapack_syevd` function will be performed.


      jobz
         Must be ``job::novec`` or ``job::vec``.


         If ``jobz = job::novec``, then only eigenvalues are computed.


         If ``jobz = job::vec``, then eigenvalues and eigenvectors are
         computed.


      upper_lower
         Must be ``uplo::upper`` or ``uplo::lower``.


         If ``upper_lower = job::upper``, a stores the upper triangular
         part of ``A``.


         If ``upper_lower = job::lower``, a stores the lower triangular
         part of ``A``.


      n
         The order of the matrix ``A`` (``0≤n``).


      lda
         The leading dimension of a. Currently lda is not referenced in
         this function.


   .. container:: section


      .. rubric:: Throws
         :class: sectiontitle


      onemkl::lapack::exception
         Exception is thrown in case of incorrect argument value is supplied.
         Position of wrong argument can be determined by `get_info()` method of exception object.


   .. container:: section


      .. rubric:: Return Value
         :class: sectiontitle


      The number of elements of type T the scratchpad memory to be passed to :ref:`onemkl_lapack_syevd` function should be able to hold.


.. container:: familylinks


   .. container:: parentlink


      **Parent topic:** :ref:`onemkl_lapack-singular-value-eigenvalue-routines` 


