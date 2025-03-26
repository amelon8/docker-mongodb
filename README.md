# docker-mongodb
See https://www.mongodb.com/docs/manual/tutorial/install-mongodb-enterprise-with-docker/

# Bring up MongoDB server

    % docker-compose up -d

# Connect to DB locally (run mongo shell in docker container)

    % docker-compose exec db bash
    
    docker$ mongosh
    
    test> db.runCommand(
    ...    {
    ...       hello: 1
    ...    }
    ... )
    {
      isWritablePrimary: true,
      topologyVersion: {
        processId: ObjectId('67e3468a331ad5eb1489cca4'),
        counter: Long('0')
      },
      maxBsonObjectSize: 16777216,
      maxMessageSizeBytes: 48000000,
      maxWriteBatchSize: 100000,
      localTime: ISODate('2025-03-26T00:13:43.648Z'),
      logicalSessionTimeoutMinutes: 30,
      connectionId: 4,
      minWireVersion: 0,
      maxWireVersion: 21,
      readOnly: false,
      ok: 1
    }

    test> show databases;
    admin   40.00 KiB
    config  12.00 KiB
    local   40.00 KiB

# Connect to DB remotely
Install Mongo Shell (e.g., run `brew install mongosh` on macOS).

    % mongosh mongodb://localhost:27017

# MongoDB admin UI
Install Mongo Compass. Refer to https://www.mongodb.com/try/download/compass

# MongoDB tutorial for beginners
https://www.w3schools.com/mongodb/

