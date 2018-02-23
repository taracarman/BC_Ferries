# BC_Ferries
Data and analysis of BC Ferries reservations data in 2016
The raw data file is how the data was received by CBC News from BC Ferries.
The clean data file adds separate columns for sailing dates and times as well as several calculated fields. Column names have been changed so that they can be analyzed in Python. 

Notes on this data from BC Ferries:

• Capacity Utilization - Each vessel’s capacity is determined using our standard Automobile Equivalent (AEQ) measurement, which is based on a standard vehicle measure of 6.1 x 2.6 metres, roughly equal to a full size family vehicle.  To determine capacity used by each sailing, the sailing’s vehicle counts are converted into the AEQ measurement, and then divided by the vessel’s full AEQ capacity.

Vessel capacity utilization percentage is based on AEQ measurements that reflect the average deck space consumed by vehicle types.  This means, in actuality, that deck space consumed on a sailing may vary from the AEQ conversion rate based on the actual size of the vehicles and how they are loaded.  Therefore, the capacity utilization percentages are an estimate of how full the sailings were and may show in the spreadsheet as exceeding full vessel capacity.

• Estimate of Overloaded Vehicles - BC Ferries does not track the number of sailing waits by individual sailing, but the number of vehicles that were left behind within the terminal compound, and a visual estimate of number of vehicles outside the terminal.  Based on this, we have produced the estimated “overload count” by sailing.

• % of Private Vehicles Carried with a Redeemed Reservation - BC Ferries does not track the number of private vehicle reservations on the Tsawwassen – Southern Gulf Islands route (route 9) because it is 100% reservable when travel is purchased in advance and the reservation is included in the fare.  There are differences between reservations made and reservations redeemed.  We have provided the data showing the percentage of private vehicles by sailing with a redeemed reservation for that particular sailing.  However, please note the following:

- Reserved vehicles that arrive outside the check-in time permitted by the reservation (i.e., the vehicle arrives early, before the reservation ‘check-in’ time or late, after the reservation ‘cut-off’ time), will either be marked as redeemed against the original sailing or as unredeemed.  In either case, they will be put in the standby (i.e., non-reserved) queue and will travel on the next sailing that can accommodate them.
- Reserved vehicles that arrive on time for a sailing which has been delayed or cancelled and then travel on a subsequent sailing will also be recorded as redeemed against the original sailing.

In some cases, subsequent to checking in and their reservation being redeemed, a customer may choose to leave the terminal, for example when there are delays due to weather or a mechanical issue.  When this occurs, the redeemed reservation would not be cancelled.  You can find information regarding reservations on the BC Ferries website at:  https://www.bcferries.com/res/visc_faq.html  

Certain circumstances produce unusual results with the data.  For example, you will see that on October 14, 2016, the scheduled 9PM sailing from Tsawwassen to Swartz Bay indicates that 1250% private vehicles had redeemed reservations.  The reason for this is as follows:

- Sailings were being delayed on the day due to weather, and the scheduled 7PM sailing’s actual departure time was 9:29PM.
- As a result, the private vehicles with reservations on the scheduled 9PM sailing instead traveled on the behind-schedule 7PM sailing which had room for them.  In effect, the reservations were marked as redeemed against the original 9PM sailing, but travelled on the earlier scheduled 7PM sailing.
- As more reservations were redeemed against the 9PM sailing than private vehicles that were actually carried on it, the mathematical result was greater than 100%.

• Delay Reason and Cancel Reason - The sailings with overloads and separately, the sailings which were delayed or cancelled with accompanying reasons such as a mechanical failure or weather.

