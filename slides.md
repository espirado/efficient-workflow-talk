---
theme: seriph
class: text-center
highlighter: Prism
lineNumbers: false
info: |
  ## Building Resilient and scalable High-Throughput  workflows Pipelines 
drawings:
  persist: false

layout: cover
---
<!--
  Happy to share how  efficient workflow pipelines can help accelerate your analysis 
-->

# Building Resilient and scalable High-Throughput Workflow Pipelines 
Efficient  orchestrating computational pipelines for complex analysis  while handling large volumes of data across heterogeneous computational environments. From low cost computational resources to high performance environments,modularity and structure of your code plays a critical role on  resource utilization . Using workflows helps orchastrate your code and  take advatange of distributed computing environments.  

---

# Agenda

<!-- global-top.vue -->

* About me
* Workflow Management system
* Modularity
* Robustness
* Reproducibility
* Interoperbilty


---

# About Me

* Andrew Espira
* Research software engineer 
* Interested in cloud Native solutions, Observability and monitoring, distributed computing, cloud engineering ,DevOps and SRE 
* Advocate for  open source community
* Football fan 

---

# Some notes

* Feel free to reach out and ask any question
* Slides & code on GitHub

---

# Workflow Management system


<v-clicks>
Automating computational analysis by linkiing together Data mananipulation/processing tasks into a cohesive pipeline. Utilizing workflow management systems like Targets, Luigi, Ruigi or Nextflow can help in defining, scheduling, and monitoring workflows. They also provide mechanisms for error handling and retrying failed tasks.

-  Whenever possible, tasks that are independent of each other should be run in parallel to reduce overall execution time
-  Processing the ever increasing data is driving the evolution of software to automate and parallelize analysis on hpc environments
-  Regularly profiling your code to identify bottlenecks and optimizing those sections can lead to better resource utilization and faster execution times.



</v-clicks>
---

# Scalability
Scalability in high-throughput workflow pipelines involves ensuring that your system can handle increasing workloads efficiently without a proportional increase in cost or time . Effective resource utilization also involves minimizing idle time for computational resources. A well-designed workflow pipeline will ensure that resources are seldom idle, thus getting the most value out of the infrastructure.
<v-clicks>

  - Time and cost of analysis tradeof- As the number of parallel tasks increases, the time to complete the overall workflow should ideally decrease. However, this is often balanced against the cost, as running many tasks in parallel may require more expensive or additional resources.

  - How your system scales with number of parallel tasks - The workflow management system should efficiently queue tasks and manage the distribution of these tasks to available resources without manual intervention.

  - How well your system distributes tasks i.e allocate RAM and Core with requirements of tasks - The system should intelligently allocate tasks based on their requirements. For instance, tasks that are memory-intensive should be allocated more RAM, while compute-intensive tasks may require more CPU cores. 
  


</v-clicks>
---

#  Modularity
Modularity in workflow pipelines is about creating a system where components or modules can be easily reused, replaced, or modified without affecting other parts of the system. This approach not only aids in scalability but also in maintainability and flexibility. 

<v-clicks>

- Build a library of reusable modules -  Design self-contained modules that perform specific tasks and can be reused across different workflows.

- Perform different analysis without refactoring code - Create generic modules that can be configured with parameters to perform different types of analyses. This way, the same module can be used for various purposes without changing the underlying code.

- Checkpoints/breakpoints to restart your workflow at any stage of the run - Implement a checkpointing system that saves the state of the workflow at various stages. This allows the workflow to be restarted from the last checkpoint in case of failure, without having to start from the beginning.

</v-clicks>

---

# Robustness
Robustness in a high-throughput workflow pipeline refers to the system's ability to continue operating despite errors or failures that might occur during execution. Handling reliability involves several strategies that ensure the system can recover from failures, prevent data loss, and maintain data integrity throughout the workflow.
<v-clicks>
 
* How your system handles reliability

- Recovery and restart from failure - Implement a checkpointing mechanism as part of the workflow. This should save the state of the process after critical steps, allowing for a restart from the last known good state in case of failure

- Hardware or network failures -  Employ a distributed system design that can tolerate the failure of one or more nodes without affecting the overall system availability. Techniques such as redundancy, replication, and failover can be utilized.

- Detecting failures from logs easily - Maintain comprehensive logging and monitoring systems that can detect and alert on anomalies. This includes logging not just errors, but also performance metrics that may indicate underlying issues.

- Data loss - Ensure data integrity checks are in place, such as checksums or hashes, to detect corruption or loss during transfer or storage.

- Data streaming piping data to downstream analysis rather than saving on a file - When data streaming is part of the workflow, design the system to handle stream processing, where data is piped to downstream analysis in real-time or near-real-time instead of being saved to a file

</v-clicks>

---

# Reproducibility
Reproducibility in computational workflows is critical for ensuring that results can be independently verified and that workflows can be reliably executed across different environments

<v-clicks>

 * Reconstruct the same workflow 
- use of package  managers
      - Utilize package managers to manage the dependencies of your code. This includes specific versions of libraries and tools required to run the workflow.
      - Document the exact versions of all dependencies used in the workflow.This can be achieved by using a lock file or an environment file that package managers like pip (for Python) or npm (for Node.js) can generate.
     - Employ virtual environments to isolate the workflow’s dependencies from the system-level packages to avoid conflicts and ensure consistency.

- Container technologies -  
      - Use containerization to package the workflow along with its environment. Container technologies like Docker can encapsulate the runtime environment, ensuring that the workflow can be run on any system that supports containers without the need for environment configuration.

</v-clicks>


---


# Demo session 
  In this session we are going to demostrate how we can implement some of the best practices in running and building workflow pipelines.
  <v-clicks>
     
     - Using slurm with Targets

     - Using nextfllow pipeline for genomic

     - Achieving parallelism in distributed system in workflow

     - Running the pipelines on hybrid environment(both local and cloud)
</v-clicks>
---

# Overall objective

<v-clicks>

* Easy to use workflow

* Researcher/scientist abstraction from the worry of infrastucture and data management

* On demand and cost Efficient

* Run anywhere 



Sample Implementation pipeline

* [code at](https://github.com/aws-samples/aws-genomics-nextflow-workshop)

</v-clicks>
---

# Q&A, Links
* [GitHub repo (slides + code)](https://github.com/espirado/slidev-rkkr52)
* Catch me on [Twitter](https://twitter.com/AEspirado), [GitHub](https://github.com/espirado), [LinkedIn](https://www.linkedin.com/in/andrew-espira-20ab3a82/) - Espira


<img src="/images/large-bird-flying-over-the-ocean-at-sunset-4092799506.jpeg"/>
---
download: true
---