# Optimizing Dwell Times

After loading a dose file or running a calculation, you can optimize the dwell times from the **Optimization tab**.

**Note**: you will need a [Gurobi license](https://www.gurobi.com/misc/lp/all/do-more-with-gurobi?utm_source=google&utm_medium=cpc&utm_campaign=2026+na+googleads+search+brand&utm_content=dmwg&gad_source=1&gad_campaignid=193283256&gclid=Cj0KCQjwxvjRBhC2ARIsAI7KJa20ReSoygu-4uWPg5zbqO6z4aqos3ofLlI185u73OgnVYaF59w3W8UaApdiEALw_wcB) to run optimization calculations. The **gurobi.lic** must be stored in your local home directory. 

The Optimization Constraints table contains the parameters for your optimization equation. You can edit the parameters by double-clicking the cells:

* **Structure**: Lists the available contoured structures.
* **Target? (Y/N)**: Enter Y if the dose should be maximized (targets) or N if it should be minimized (organs at risk).
* **Dose Goal [Gy]**: The target dose for the structure, in Gray.
* **Weight**: The penalty weight parameters for the optimization algorithm.

### Standard Optimization Pipeline

1. **Select Constraints**: Right-click a structure to toggle it on or off. Shaded structures are disabled and will be ignored during optimization.
2. **Set Targets**: Define whether each active structure should receive a maximum (Y) or minimum (N) dose in the Target column.
3. **Set Goals**: Enter the target dose for each active structure.
4. **Assign Weights**: Enter the penalty weights for each structure.
5. **Run**: Click Optimize.

Once the optimization finishes, review your results in the **DVH tab**. If the results need refinement, adjust your weights and run the optimization again. The calculated dwell times will automatically update in the catheter table.

### Graphical Optimization

To perform manual graphical optimization, click the `Enable` button next to `Graphical Optimization`. You can then click and drag the isodose lines directly in the viewing panels to adjust the dose distribution. As you modify the lines, the dwell times in the catheter table will update automatically to reflect your changes.