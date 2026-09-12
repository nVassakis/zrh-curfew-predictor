# LSZH curfew predictor

*Problem* = Zurich Airport (LSZH) has a strict night curfew: departures are banned after 23:00 and delayed flights face a hard stop at 23:30. In the airline hub model, an inbound flight’s delay shrinks the ground "turnaround" window (cleaning, refueling, boarding). If a delayed inbound flight combined with poor ground weather causes the outbound flight to miss the 23:30 curfew, the flight is canceled, costing the airline tens of thousands of euros in hotel rooms and EU261 compensation.


*Solution* = An end-to-end pipeline that ingests live aircraft telemetry and weather data, calculates dynamic turnaround buffers against the airline timetable, and uses an XGBoost machine learning model to predict the probability of a curfew breach hours before the plane lands. This allows the Hub Operations Center to proactively send extra ground crew to high-risk flights to compress the turnaround time and save the flight.

