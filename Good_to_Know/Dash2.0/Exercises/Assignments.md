# Exercises to help you get started with Dash 

1. Customize the layout so the dropdown and the choropleth graph are next to each other on the page. The total width of columns inside one row must be equal or less than 12. Hint - see the second example in [Dash Bootstrap docs](https://dash-bootstrap-components.opensource.faculty.ai/docs/components/layout/).
2. Modify the app so it plots a bar graph instead of the choropleth graph. The x-axis should represent states while the y-axis should represent the `column_name` from the dropdown. See Plotly docs on [the bar chart](https://plotly.com/python/bar-charts/).    
3. Replace the bar chart or choropleth map with a line chart. The x-axis representing the year, the y-axis representing the `column_name`, and color representing the States. See Plotly docs on [the line chart](https://plotly.com/python/line-charts/). (When done, see the TEEN BIRTHS PER 1,000 trend in the graph.).
4. Take the app-with-graph.py file. Add an empty `Alert` [Dash Mantine Component](https://dash-mantine-components.herokuapp.com/components/alert) to the layout between the markdown and the graph. Insert the Alert component as the second Output in the callback, with `children` as the component property. Modify the callback function so it returns this string, `"The data for the bar graph is highly confidential."` if user chooses a bar plot, and it returns this string, `"The scatter plot is believed to have been first published in 1833"` if user chooses a scatter plot.
5. Take the interactive-app.py file. Add a [radioItems Dash Core Component](https://dash.plotly.com/dash-core-components/radioitems) to the layout after assigning the following colors to its `options` property: `['blue','red','green']`. Incorporate the RadioItems component into the callback so the button/color chosen updates the color of the markdown text. Hint - the callback will have a total of 2 Outputs and 2 Inputs. To color the Markdown text in purple, its `style` property is written like this: `dcc.Markdown(style={'color':'purple'})`