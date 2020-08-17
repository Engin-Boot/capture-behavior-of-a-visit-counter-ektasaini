# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given a backup server which stores latest visitor count
  When server goes down
  Then backup server recovers the latest visitor count and updates
  server on restart

Scenario: Reconcile counts if the sensor is offline for a while

  Given a backup server which activates when sensor goes offline
  When sensor status changes to offline
  Then the backup mechanism activates, records the count and
  reconciles counts when server is back online
