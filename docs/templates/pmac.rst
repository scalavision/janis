Pmac
====

Template ID: ``pmac``



Quickstart
-----------

Take note below how to configure the template. This quickstart only includes the fields you absolutely require. This will write a new configuration to ``~/.janis.conf``. See `configuring janis <https://janis.readthedocs.io/en/latest/references/configuration.html>`__ for more information.

.. code-block:: bash

   janis init pmac
   
   # or to find out more information
   janis init pmac --help

OR you can insert the following lines into your template:

.. code-block:: yaml

   template:
     id: pmac



Fields
-------



**Optional**

==============================  ===================================  ====================================================  ======================================================================
ID                              Type                                 Default                                               Documentation
==============================  ===================================  ====================================================  ======================================================================
execution_dir                   <class 'str'>                                                                              Execution directory
container_dir                   <class 'str'>                        /config/binaries/singularity/containers_devel/janis/  [OPTIONAL] Override the directory singularity containers are stored in
queues                          typing.Union[str, typing.List[str]]  prod_med,prod                                         The queue to submit jobs to
singularity_version             <class 'str'>                        3.4.0                                                 The version of Singularity to use on the cluster
send_job_emails                 <class 'bool'>                       False                                                 Send Slurm job notifications using the provided email
catch_slurm_errors              <class 'bool'>                       True                                                  Fail the task if Slurm kills the job (eg: memory / time)
singularity_build_instructions                                                                                             Sensible default for PeterMac template
max_cores                       <class 'int'>                        40                                                    Override maximum number of cores (default: 32)
max_ram                         <class 'int'>                        256                                                   Override maximum ram (default 508 [GB])
max_workflow_time               <class 'int'>                        20100                                                 The walltime of the submitted workflow "brain"
janis_memory_mb
==============================  ===================================  ====================================================  ======================================================================

