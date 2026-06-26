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