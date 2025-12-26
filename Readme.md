**The Project Folder Content**

CE555\_TermProject\_1908607.docx -Term Paper

CE555\_TermProject\_1908607.pptx - Presentation

CE555\_TermProject.ipynb - Data Preprocessing Operations

dataset\_3.csv – Input dataset



**Required Python Libraries**

The notebook requires the following libraries:

pandas

numpy

matplotlib.pyplot

missingno



**Data Structure**

The dataset is converted into trip-alternative (long) format:



2 rows per respondent

1 row per alternative (Mode A / Mode B)



***Key identifiers:***



**Obs\_ID – choice situation ID (one per respondent)**

**Mode – alternative indicator**

1 = Mode A

0 = Mode B

**Choice – choice indicator**

1 = chosen alternative

0 = not chosen



***Main Variables (After Data Preparation)***

Individual-specific (repeated for both alternatives)

Age

Gender (0/1)

Education

Income\_TRY

Income\_cat – income category (low / medium / high)

Working\_Status

Work\_cat – ordinal working status

Driver\_License (0/1)

Car\_Ownership (0/1)

Residence\_Center (0/1)



***Alternative-specific***

Travel\_Time – in-vehicle travel time (minutes)

Travel\_Cost – monetary cost

Wait – waiting time (Mode B only)

Transfer – number of transfers (Mode B only)

Comfort – comfort level (Mode B only)

Parking – parking availability (Mode A only)



***Derived Variables***

Driveability – 1 if license \& car ownership

ln\_time – log of travel time (diminishing disutility)

ln\_cost – log of travel cost

Perceived\_Time – constructed travel time using estimated wait/transfer weights

ln\_Perceived\_Time – log of perceived travel time



Perceived time is computed as:

Perceived\_Time = Travel\_Time + w\_wait \* Wait + p\_tr \* Transfer

where weights are calculated from estimated model coefficients, not assumed.



**Execution:** run notebook top-to-bottom for full reproduction

**Notes**

The notebook intentionally keeps intermediate variables for clarity.

Recommended environment: Google Colab (no local setup required)

