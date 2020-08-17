# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given An calender synced sensor that differentiates between patient-card and visitor-card
  When a visitor-card is detected
  Then count records for current day and updates report bar graph for week

Scenario: Alert when seating capacity is full

  Given a sensor that detects pressure and decrements the total number of seats available
  When the available seat count is zero
  Then system alerts the operator about full seating space
