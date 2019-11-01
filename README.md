# MongoChat

Simple chat app that uses MongoDB and Socket.io

### Version
1.0.0

## Install Dependencies
```bash
npm install 
```

## Run Server
```bash
npm start
```




## rs.status()
```bash
myReplSet:SECONDARY> rs.status()
{
        "set" : "myReplSet",
        "date" : ISODate("2019-10-31T07:46:57.013Z"),
        "myState" : 2,
        "term" : NumberLong(2),
        "syncingTo" : "vps3:27017",
        "syncSourceHost" : "vps3:27017",
        "syncSourceId" : 2,
        "heartbeatIntervalMillis" : NumberLong(2000),
        "majorityVoteCount" : 2,
        "writeMajorityCount" : 2,
        "optimes" : {
                "lastCommittedOpTime" : {
                        "ts" : Timestamp(1572508014, 1),
                        "t" : NumberLong(2)
                },
                "lastCommittedWallTime" : ISODate("2019-10-31T07:46:54.157Z"),
                "readConcernMajorityOpTime" : {
                        "ts" : Timestamp(1572508014, 1),
                        "t" : NumberLong(2)
                },
                "readConcernMajorityWallTime" : ISODate("2019-10-31T07:46:54.157Z"),
                "appliedOpTime" : {
                        "ts" : Timestamp(1572508014, 1),
                        "t" : NumberLong(2)
                },
                "durableOpTime" : {
                        "ts" : Timestamp(1572508014, 1),
                        "t" : NumberLong(2)
                },
                "lastAppliedWallTime" : ISODate("2019-10-31T07:46:54.157Z"),
                "lastDurableWallTime" : ISODate("2019-10-31T07:46:54.157Z")
        },
        "lastStableRecoveryTimestamp" : Timestamp(1572507984, 1),
        "lastStableCheckpointTimestamp" : Timestamp(1572507984, 1),
        "members" : [
                {
                        "_id" : 0,
                        "name" : "vps1:27017",
                        "ip" : "172.31.47.98",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 38388,
                        "optime" : {
                                "ts" : Timestamp(1572508014, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-10-31T07:46:54Z"),
                        "syncingTo" : "vps3:27017",
                        "syncSourceHost" : "vps3:27017",
                        "syncSourceId" : 2,
                        "infoMessage" : "",
                        "configVersion" : 1,
                        "self" : true,
                        "lastHeartbeatMessage" : ""
                },
                {
                        "_id" : 1,
                        "name" : "vps2:27017",
                        "ip" : "172.31.37.103",
                        "health" : 1,
                        "state" : 1,
                        "stateStr" : "PRIMARY",
                        "uptime" : 4166,
                        "optime" : {
                                "ts" : Timestamp(1572508014, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572508014, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-10-31T07:46:54Z"),
                        "optimeDurableDate" : ISODate("2019-10-31T07:46:54Z"),
                        "lastHeartbeat" : ISODate("2019-10-31T07:46:56.759Z"),
                        "lastHeartbeatRecv" : ISODate("2019-10-31T07:46:56.571Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "electionTime" : Timestamp(1572469623, 1),
                        "electionDate" : ISODate("2019-10-30T21:07:03Z"),
                        "configVersion" : 1
                },
                {
                        "_id" : 2,
                        "name" : "vps3:27017",
                        "ip" : "172.31.33.232",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 35539,
                        "optime" : {
                                "ts" : Timestamp(1572508014, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572508014, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-10-31T07:46:54Z"),
                        "optimeDurableDate" : ISODate("2019-10-31T07:46:54Z"),
                        "lastHeartbeat" : ISODate("2019-10-31T07:46:56.758Z"),
                        "lastHeartbeatRecv" : ISODate("2019-10-31T07:46:56.571Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "vps2:27017",
                        "syncSourceHost" : "vps2:27017",
                        "syncSourceId" : 1,
                        "infoMessage" : "",
                        "configVersion" : 1
                }
        ],
        "ok" : 1,
        "$clusterTime" : {
                "clusterTime" : Timestamp(1572508014, 1),
                "signature" : {
                        "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
                        "keyId" : NumberLong(0)
                }
        },
        "operationTime" : Timestamp(1572508014, 1)
}
```
## rs.config() 
```bash
myReplSet:SECONDARY> rs.config()
{
        "_id" : "myReplSet",
        "version" : 1,
        "protocolVersion" : NumberLong(1),
        "writeConcernMajorityJournalDefault" : true,
        "members" : [
                {
                        "_id" : 0,
                        "host" : "vps1:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 1,
                        "host" : "vps2:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 2,
                        "host" : "vps3:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                }
        ],
        "settings" : {
                "chainingAllowed" : true,
                "heartbeatIntervalMillis" : 2000,
                "heartbeatTimeoutSecs" : 10,
                "electionTimeoutMillis" : 10000,
                "catchUpTimeoutMillis" : -1,
                "catchUpTakeoverDelayMillis" : 30000,
                "getLastErrorModes" : {

                },
                "getLastErrorDefaults" : {
                        "w" : 1,
                        "wtimeout" : 0
                },
                "replicaSetId" : ObjectId("5db9e7356c259daeb8e7e975")
        }
}
```
![](https://github.com/donrast41/Lab9/blob/master/IMAGE%202019-11-01%2012:29:06.jpg)

## After removing vps

### rs.status()
```bash
myReplSet:PRIMARY> rs.status()
{
        "set" : "myReplSet",
        "date" : ISODate("2019-10-31T07:54:07.054Z"),
        "myState" : 1,
        "term" : NumberLong(3),
        "syncingTo" : "",
        "syncSourceHost" : "",
        "syncSourceId" : -1,
        "heartbeatIntervalMillis" : NumberLong(2000),
        "majorityVoteCount" : 2,
        "writeMajorityCount" : 2,
        "optimes" : {
                "lastCommittedOpTime" : {
                        "ts" : Timestamp(1572508445, 1),
                        "t" : NumberLong(3)
                },
                "lastCommittedWallTime" : ISODate("2019-10-31T07:54:05.182Z"),
                "readConcernMajorityOpTime" : {
                        "ts" : Timestamp(1572508445, 1),
                        "t" : NumberLong(3)
                },
                "readConcernMajorityWallTime" : ISODate("2019-10-31T07:54:05.182Z"),
                "appliedOpTime" : {
                        "ts" : Timestamp(1572508445, 1),
                        "t" : NumberLong(3)
                },
                "durableOpTime" : {
                        "ts" : Timestamp(1572508445, 1),
                        "t" : NumberLong(3)
                },
                "lastAppliedWallTime" : ISODate("2019-10-31T07:54:05.182Z"),
                "lastDurableWallTime" : ISODate("2019-10-31T07:54:05.182Z")
        },
        "lastStableRecoveryTimestamp" : Timestamp(1572508407, 1),
        "lastStableCheckpointTimestamp" : Timestamp(1572508407, 1),
        "electionCandidateMetrics" : {
                "lastElectionReason" : "stepUpRequestSkipDryRun",
                "lastElectionDate" : ISODate("2019-10-31T07:52:14.503Z"),
                "termAtElection" : NumberLong(3),
                "lastCommittedOpTimeAtElection" : {
                        "ts" : Timestamp(1572508334, 1),
                        "t" : NumberLong(2)
                },
                "lastSeenOpTimeAtElection" : {
                        "ts" : Timestamp(1572508334, 1),
                        "t" : NumberLong(2)
                },
                "numVotesNeeded" : 2,
                "priorityAtElection" : 1,
                "electionTimeoutMillis" : NumberLong(10000),
                "priorPrimaryMemberId" : 1,
                "numCatchUpOps" : NumberLong(27017),
                "newTermStartDate" : ISODate("2019-10-31T07:52:15.178Z"),
                "wMajorityWriteAvailabilityDate" : ISODate("2019-10-31T07:52:16.046Z")
        },
        "members" : [
                {
                        "_id" : 0,
                        "name" : "vps1:27017",
                        "ip" : "172.31.47.98",
                        "health" : 1,
                        "state" : 1,
                        "stateStr" : "PRIMARY",
                        "uptime" : 38818,
                        "optime" : {
                                "ts" : Timestamp(1572508445, 1),
                                "t" : NumberLong(3)
                        },
                        "optimeDate" : ISODate("2019-10-31T07:54:05Z"),
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "electionTime" : Timestamp(1572508334, 2),
                        "electionDate" : ISODate("2019-10-31T07:52:14Z"),
                        "configVersion" : 1,
                        "self" : true,
                        "lastHeartbeatMessage" : ""
                },
                {
                        "_id" : 1,
                        "name" : "vps2:27017",
                        "ip" : "172.31.37.103",
                        "health" : 0,
                        "state" : 8,
                        "stateStr" : "(not reachable/healthy)",
                        "uptime" : 0,
                        "optime" : {
                                "ts" : Timestamp(0, 0),
                                "t" : NumberLong(-1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(0, 0),
                                "t" : NumberLong(-1)
                        },
                        "optimeDate" : ISODate("1970-01-01T00:00:00Z"),
                        "optimeDurableDate" : ISODate("1970-01-01T00:00:00Z"),
                        "lastHeartbeat" : ISODate("2019-10-31T07:54:06.108Z"),
                        "lastHeartbeatRecv" : ISODate("2019-10-31T07:52:14.596Z"),
                        "pingMs" : NumberLong(1),
                        "lastHeartbeatMessage" : "Error connecting to vps2:27017 (172.31.37.103:27017) :: caused by :: No route to host",
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "configVersion" : -1
                },
                {
                        "_id" : 2,
                        "name" : "vps3:27017",
                        "ip" : "172.31.33.232",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 35969,
                        "optime" : {
                                "ts" : Timestamp(1572508445, 1),
                                "t" : NumberLong(3)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572508445, 1),
                                "t" : NumberLong(3)
                        },
                        "optimeDate" : ISODate("2019-10-31T07:54:05Z"),
                        "optimeDurableDate" : ISODate("2019-10-31T07:54:05Z"),
                        "lastHeartbeat" : ISODate("2019-10-31T07:54:06.519Z"),
                        "lastHeartbeatRecv" : ISODate("2019-10-31T07:54:06.063Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "vps1:27017",
                        "syncSourceHost" : "vps1:27017",
                        "syncSourceId" : 0,
                        "infoMessage" : "",
                        "configVersion" : 1
                }
        ],
        "ok" : 1,
        "$clusterTime" : {
                "clusterTime" : Timestamp(1572508445, 1),
                "signature" : {
                        "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
                        "keyId" : NumberLong(0)
                }
        },
        "operationTime" : Timestamp(1572508445, 1)
}
```
## rs.config()
```bash
myReplSet:PRIMARY> rs.config()
{
        "_id" : "myReplSet",
        "version" : 1,
        "protocolVersion" : NumberLong(1),
        "writeConcernMajorityJournalDefault" : true,
        "members" : [
                {
                        "_id" : 0,
                        "host" : "vps1:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 1,
                        "host" : "vps2:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 2,
                        "host" : "vps3:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                }
        ],
        "settings" : {
                "chainingAllowed" : true,
                "heartbeatIntervalMillis" : 2000,
                "heartbeatTimeoutSecs" : 10,
                "electionTimeoutMillis" : 10000,
                "catchUpTimeoutMillis" : -1,
                "catchUpTakeoverDelayMillis" : 30000,
                "getLastErrorModes" : {

                },
                "getLastErrorDefaults" : {
                        "w" : 1,
                        "wtimeout" : 0
                },
                "replicaSetId" : ObjectId("5db9e7356c259daeb8e7e975")
        }
}
```
![](https://github.com/donrast41/Lab9/blob/master/IMAGE%202019-11-01%2012:29:08.jpg)
