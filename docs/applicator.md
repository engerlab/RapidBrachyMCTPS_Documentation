# Applicators
If you have an applicator STL to place, you can do so through the RapidBrachy module's **Applicator tab**. 

## Importing Applicator
Click `Applicator STL Directory` and select the folder with your applicator STL files. Under `Applicator Template JSON`, enter the path to your applicator template JSON file. 

#### Applicator Template JSON
The Applicator Template JSON file acts as a blueprint that provides RapidBrachyMCTPS with the 3D geometry, catheter routing, and source dwell parameters needed to simulate a specific brachytherapy applicator.

Below is a template for the applicator JSON file. Replace the placeholders values (for exmaple <FLOAT\>, <INTEGER\>, and <STRING\>) with your own data.

```json
{
    "catheters_dict": {
        "<CATHETER_ID_STRING>": {
            "index": <INTEGER>,
            "dwells": [
                {
                    "index": <INTEGER>,
                    "name_id": "<STRING_IDENTIFIER>",
                    "catheter_index": <INTEGER>,
                    "angle": <FLOAT>,
                    "position": [
                        <FLOAT_X>,
                        <FLOAT_Y>,
                        <FLOAT_Z>
                    ],
                    "relativePos": <FLOAT>,
                    "rotation": [
                        <FLOAT_X>,
                        <FLOAT_Y>,
                        <FLOAT_Z>
                    ],
                    "time": <FLOAT>,
                    "weight": <FLOAT>
                }
            ],
            "tip_position": [
                <FLOAT_X>,
                <FLOAT_Y>,
                <FLOAT_Z>
            ],
            "last_dwell_coordinate": [
                <FLOAT_X>,
                <FLOAT_Y>,
                <FLOAT_Z>
            ],
            "step_size": <FLOAT>,
            "digitization_points": [
                [
                    <FLOAT_X>,
                    <FLOAT_Y>,
                    <FLOAT_Z>
                ],
                [
                    <FLOAT_X>,
                    <FLOAT_Y>,
                    <FLOAT_Z>
                ]
            ],
            "afterloader_channel_number": <INTEGER>,
            "insert_position": <NULL_OR_ARRAY_OF_3_FLOATS>,
            "channel_total_time": <FLOAT>,
            "channel_length": <NULL_OR_FLOAT>
        }
    },
    "step_size": <FLOAT>,
    "treatment_time": <FLOAT>
}
```

## Placing Applicator
After loading, the applicator will appear in the viewing panels. You can adjust its location and orientation using the center dot and rotation wheel.

Once properly positioned, click `Lock Applicator` to automatically populate the catheter table with the dwell positions. If you need to make further adjustments, click `Unlock Applicator`; note that this action will clear the current dwell positions from the table.

## Shielded Applicator
### To make the applicator shielded for Intensity Modulated BrachyTherapy (IMBT)

1. Navigate to RapidBrachy module's **Catheter tab**. Under `Catheter Operations`, select the catheter(s) that should be shielded. 
2. Select the starting angle (with respect to the applicator's current placement), the stopping angle, and the step size in degrees.
3. Click `Make Shielded`. This will populate your catheter table with dwell positions for each individual angle.

**Note: If you are running TG-43 simulations, use the TG-43S algorithm instead of the standard TG-43.**