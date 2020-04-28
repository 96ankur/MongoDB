- MONGODB CONVERT "JSON" FORMAT TO ANOTHER FORMAT FOR STORING, CALLED "BSON" (it is binary version of json and 
  can queried more efficiently).

### CHARACTERISTICS OF MONGODB ###
 - No Schema
 - No/Few Relations

```js
                                        WORKING WITH MONGODB
                                                                                                        ______    
            APPLICATION                        Queries                          DATA                    |    |
    Frontend     Backend ----> Driver --------------------------->   Mongodb <----> Storage  <------>   |    |
       (UI)      (server)       (NodeJs)                            (server)         Engine             |____|
                                                                      ^     Communication     File/Data  
                                                                      |                         Access
                                                                      |
                                                                      |
                                                                      |
                        MongoDB Shell ---------------------------------
```
- Default Storage Engine is "Wired Tiger"
- Storage Engine loads a chunk of data into memory and manages to store the data in memory that is used frequently.



```js
                                                                ______
                                        DATA                    |    |
                             Mongodb <----> Storage  <------>   |    |  Read + Write Data in Files (slow)
                            (server)         Engine             |____|
                                                ^
                                                |       _________
                                                |       |       |
                                                |_______| memory|  Read + Write Data in Memory(fast)
                                                        |_______|
```
- In mongoDB, there are a number of databases and these databases has a number of collections and each collection contians a number of document.

```js
                           _____________________________
                            |        Databases          |
                            |   ______________________  |
                            |  |     Collections     |  |
                            |  |  __________________ |  |
                            |  | |   Documents     | |  |
                            |  | |_________________| |  |
                            |  |_____________________|  |
                            |___________________________|
```