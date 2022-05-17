# Understand TEQ

## Introduction

Transactional Event Queues(TEQ) samples to create queues using different payloads, Enqueue, dequeue, and cleanups using PL/SQL.

- Estimated Time: 10 minutes

### Objectives

- Create Transactional Event Queue
- Enqueue Transactional Event Queue
- Dequeue Transactional Event Queue

### Prerequisites

- This workshop assumes you have an Oracle cloud account and configured setup in Lab 1.

## Task 1: Create TEQ, Enqueue, Dequeue and Cleanup using PLSQL

1. Below are the code samples to create TEQ

    ![teqCreate](./images/create-teq.png " ")

    - Execute the following sequence of commands into cloud shell

        ```bash
        <copy>cd $ORACLETEQ_HOME/TEQPlsql; source createTEQ.sh;
        </copy>
        ```

2. Below are the code samples to Enqueue TEQ:

    ![enqueueTEQ](./images/enqueue-teq.png " ")

    - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PLSQL_TEQ; source enqueueTEQ.sh;
        </copy>
        ```

3. Below are the code samples to Dequeue TEQ

    ![dequeueTEQ](./images/dequeue-teq.png " ")

    - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PLSQL_TEQ; source dequeueTEQ.sh;
        </copy>
        ```

4. Below are the code samples to cleanup TEQ

    - Stop Queues

    - Drop Queues

    - Drop Queue Tables

    ![cleanupTEQ](./images/cleanup-teq.png " ")

    - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PLSQL_TEQ; source cleanupTEQ.sh;
        </copy>
        ```

## Task 2: TEQ Enqueue and Dequeue using Java

1. Execute the following sequence of commands into cloud shell

    ```bash
    <copy> curl http://localhost:8081/oracleTEQ/pubSubTEQ </copy>
    ```

    You can view the source code for this lab [here.](https://github.com/oracle/microservices-datadriven/tree/main/workshops/oracleTEQ/qJava/src/main/java/com/examples/enqueueDequeueTEQ/EnqueueDequeueTEQ.java)

## Task 3: Create Queues, Enqueue, Dequeue and cleanup using Python

1. Create TEQ 

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PYTHON_TEQ; python3.6 pythonCreateTEQ.py;
        </copy>
        ```

2. Enqueue, Dequeue TEQ for Payload as ADT, RAW and JMS

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PYTHON_TEQ; pyhton3.6 pythonEnqDeqTEQ.py;
        </copy>
        ```

3. Clean up for Python TEQ

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $PYTHON_TEQ; python3.6 pythonCleanupTEQ.py;
        </copy>
        ```

## Task 4: Create Queues, Enqueue, Dequeue and Cleanup using Node.js

1. Create TEQ

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $NODE_TEQ; node nodeCreateTEQ.js;
        </copy>
        ```

2. Enqueue, Dequeue TEQ for Payload ADT, RAW

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $NODE_TEQ; node nodeEnqDeqTEQ.js;
        </copy>
        ```

3. Clean up TEQ

      - Execute the following sequence of commands into cloud shell:

        ```bash
        <copy>cd $NODE_TEQ; node nodeEnqDeqTEQ.js;
        </copy>
        ```

You may now **proceed to the next lab.**

## Acknowledgements

- **Author** - Mayank Tayal, Developer Advocate
- **Contributors** - Sanjay Goil, VP Microservices and Oracle Database; Paul Parkinson, Developer Evangelist; Paulo Simoes, Developer Evangelist; Richard Exley, Maximum Availability Architecture; Shivani Karnewar, Senior Member Technical Staff
- **Last Updated By/Date** - Mayank Tayal, February 2022
