# Understand Advanced Queues

## Introduction

This lab will give an understanding of Advanced Queues creation using different payloads, enqueue AQ, dequque AQ, and cleanups.

- Estimated Time: 10 minutes

### Objectives

- Create Advanced Queues
- Enqueue for Advanced Queues
- Dequeue for Advanced Queues

### Prerequisites

- This workshop assumes you have an Oracle cloud account and configured setup in Lab 1.

## Task 1: Create AQ, Enqueue, Dequeue and Cleanup using PL/SQL

1. Below are the code samples to create AQ:

    - Single consumer 

    - Multi-Consumer 

        ![createAQ](./images/create-aq.png " ")

    - Execute the following sequence of commands into cloud shell:  

        ```bash
        <copy>cd $PLSQL_AQ; source createAQ.sh;
        </copy>
        ```

2. Below are the code samples to Enqueue AQ:

    ![enqueueAQ](./images/enqueue-aq.png " ")

    - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PLSQL_AQ; source enqueueAQ.sh;
        </copy>
        ```

3. Below are the code samples to dequeue AQ

    ![dequeueAQ](./images/dequeue-aq.png " ")

    - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PLSQL_AQ; source dequeueAQ.sh;
        </copy>
        ```

4. Below are the code samples to cleanup AQ

    - Stop Queues

    - Drop Queues

    - Drop Queue Tables

        ![cleanupAQ](./images/cleanup-aq.png " ")

    - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PLSQL_AQ; source cleanupAQ.sh;
        </copy>
        ```

## Task 2: Create AQ, Enqueue, Dequeue and Cleanup using Java

1. Point to Point
    - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy> curl http://localhost:8081/oracleAQ/pointToPointAQ 
        </copy>
        ```

2. Publisher Subscriber
    - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy> curl http://localhost:8081/oracleAQ/pubSubAQ 
        </copy>
        ```

    You can view the source code for this lab [here.](https://github.com/oracle/microservices-datadriven/tree/main/workshops/oracleAQ/qJava/src/main/java/com/examples/enqueueDequeueAQ/EnqueueDequeueAQ.java)

## Task 3: Create Queues, Enqueue, Dequeue and cleanup using Python

1. Create AQ 

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PYTHON_AQ; python3.6 pythonCreateAQ.py;
        </copy>
        ```

2. Enqueue, Dequeue AQ for Payload as ADT, RAW and JMS

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PYTHON_AQ; pyhton3.6 pythonEnqDeqAQ.py;
        </copy>
        ```

3. Clean up for Python AQ

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PYTHON_AQ; python3.6 pythonCleanupAQ.py;
        </copy>
        ```

## Task 4: Create Queues, Enqueue, Dequeue and Cleanup using Node.js

1. Create AQ

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $NODE_AQ; node nodeCreateAQ.js;
        </copy>
        ```

2. Enqueue, Dequeue AQ for Payload ADT, RAW

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $NODE_AQ; node nodeEnqDeqAQ.js;
        </copy>
        ```

3. Clean up AQ

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $NODE_AQ; node nodeEnqDeqAQ.js;
        </copy>
        ```

You may now **proceed to the next lab.**

## Acknowledgements

- **Author** - Mayank Tayal, Developer Advocate
- **Contributors** - Sanjay Goil, VP Microservices and Oracle Database; Paul Parkinson, Developer Evangelist; Paulo Simoes, Developer Evangelist; Richard Exley, Maximum Availability Architecture; Shivani Karnewar, Senior Member Technical Staff
- **Last Updated By/Date** - Mayank Tayal, February 2022
