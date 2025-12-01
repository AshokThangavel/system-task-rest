
## Installation 

Clone/git pull the repo into any local directory

```
$ git clone https://github.com/AshokThangavel/system-task-rest.git
```

go to directory
```
$ cd system-task-rest
```

Open the terminal in this directory and run:

```
$ docker-compose build
```

3. Run the IRIS container with your project:

```
$ docker-compose up -d
```

Get System task details in REST service

**Task information urls**
List of urls
1. Get all task list
   `http://localhost:52773/zsystemtasks/task/alltask`

2. filter task details by namespace, taskname etc... (Use SYS instead of %SYS)
    `http://localhost:52773/zsystemtasks/task/alltask/SYS`

3. Get list of upcoming task details
   `http://localhost:52773/zsystemtasks/task/upcomingtask`

4. Get list of on-demand task
   `http://localhost:52773/zsystemtasks/task/ondemandtask`

5. Get entire task history
     `http://localhost:52773/zsystemtasks/task/taskhistory`

6. Get task history for specific task
  `http://localhost:52773/zsystemtasks/task/taskhistory/taskname`

**Sample response**
```json[
    {
        "Last Start": "2023-08-21 09:17",
        "Completed": "2023-08-21 09:17",
        "Task Name": "ExportQueryToCSV",
        "Status": "1",
        "Result": "Success",
        "Task": "1001",
        "NameSpace": "LEARNING",
        "Routine": "Samples.TaskMgr.SQLExportTask",
        "Pid": "14188",
        "%ER Date": "",
        "%ER Error #": "",
        "Username": "_SYSTEM",
        "LogDate": "2023-08-21",
        "LogTime": "33446"
    }
  ]
  ```


## How to Test it

Run the various URLs from your Browser or Postman or similar

**database information urls**
1. Get database freespace
   http://server:port/crud/database/freespace     (http://localhost:52773/zsystemtasks/database/freespace)
   ![image](https://github.com/AshokThangavel/System-Task-REST/assets/58914152/2488832b-fd77-422f-a914-4abc7b8c70e3)
