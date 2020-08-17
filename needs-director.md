# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given A calender synced sensor that differentiates between patient-card and non-patient-card
  When There is an entry, sensor identifies the type of card
  Then Based on number of different patient-cards sensed, sensor reports it

Scenario: Compute parking slots to reserve for visiting specialists

  Given  a sensor to detect incoming of specialists car
  through it's number and the empty slots are there
  When a specialist is visiting the hospital Then reserve the slot for him/her
