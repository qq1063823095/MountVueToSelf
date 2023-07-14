# Use
The script is used in the Tampermonkey plugin to import the Vue framework using the "@require" method.

# Explain
Some third-party frameworks (e.g., Element Plus) depend on the Vue framework. When these frameworks are imported using the "@require" method due to the limitations of the Tampermonkey plugin execution, it becomes impossible to pass the Vue object into the framework. As a result, an error occurs indicating that the Vue object does not exist, as shown in the screenshot.

![Alternative frameworks access the Vue instance within the window](./Images/Alternative%20frameworks%20access%20the%20Vue%20instance%20within%20the%20window.png)
![Function for executing scripts in Tampermonkey](./Images/Function%20for%20executing%20scripts%20in%20Tampermonkey.png)


# Other
Question: Why not directly bundle the frameworks into the script using tools like WebPack or Vite?
Answer: The final bundled code would be large, causing the Tampermonkey plugin to become unresponsive and unusable.