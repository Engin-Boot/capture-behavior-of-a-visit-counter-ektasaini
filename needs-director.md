# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given  A calender synced sensor that differentiates between patient-card and non-patient-card
  When There is an entry, sensor identifies the type of card
  Then increments the patient-card enteries on that particular day

Scenario: Compute parking slots to reserve for visiting specialists

  Given
  When
  Then
