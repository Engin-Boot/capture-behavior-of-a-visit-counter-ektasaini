# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given server has a real time backup available which stores
  latest visitor count
  When server goes down
  Then real time backup recovers latest visitor count and updates
  server on restart

Scenario: Reconcile counts if the sensor is offline for a while

  Given sensor has a backup mechanism which activates when sensor
  goes offline
  When sensor status changes to offline
  Then the backup mechanism activates, records the count and
  reconciles counts when server is back online
