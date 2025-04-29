# Viewing Data as the Visiting User in Streamlit in Snowflake

This repo contains a Snowflake Notebook (`.ipynb`) file that can 
be imported into Snowflake. It walks through an example of how to
use the `READ SESSION` permission to give a Streamlit access to the
context functions for the visiting user (e.g., `CURRENT_USER()` or 
`CURRENT_AVAILABLE_ROLES()`). These context functions can then be 
used in Row Access Policies (RAPs) that will restrict the data that
is visible when queried. Using this `READ SESSION` permission along
with RAPs that leverage the context functions allows a Streamlit
to query data in Snowflake with the access of the visiting user.

The example leverages an entitlement table to set which rows are
visible to which users.

## Instructions
To follow this example, download the `StreamlitRAP.ipynb` file
(or alternatively, clone this repository). Then, in Snowflake,
in the Notebook page, click the down arrow next to the 
"+ Notebook" button in the upper right, choose "Import .ipynb file", 
and select the `StreamlitRAP.ipynb` file. Then fill out the rest of 
the details (location, Python environment, etc).

Then just follow along the instructions inside the Notebook.