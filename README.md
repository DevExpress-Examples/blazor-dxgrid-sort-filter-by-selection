<!-- default badges list -->
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T1273428)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->
# Blazor Grid — Sort and Filter Data by Selection

The [DevExpress Blazor Grid](https://docs.devexpress.com/Blazor/403143/components/grid) component allows users to sort/filter data against multiple data columns. This example extends built-in capabilities and sorts/filters the Grid by selected rows.

Sorting and filtering by selection helps when no simple filter criteria can identify all necessary records. Consider a situation when a user needs to display only tasks relevant to today’s activities. These tasks belong to different categories, have different priorities, and due dates. In such instances, users can select all relevant records and then bring them to the top or display only those records on screen.

![Sort and Filter Data by Selection](sort-and-filter-grid-by-selection.gif)

## Implementation Details

To filter [DevExpress Blazor Grid](https://docs.devexpress.com/Blazor/403143/components/grid) against selected rows, assign [SelectedDataItems](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid.SelectedDataItems) to the [Data](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid.Data) property. To sort grid data against selections, create a service column as follows:

1. Add an [invisible](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGridColumn.Visible) column to the Grid component.
2. Set the column's [FieldName](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGridDataColumn.FieldName) to a unique value not present in the bound data source.
3. Set the column's [UnboundType](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGridDataColumn.UnboundType) to a value other than `Bound`.
4. Set the column's [SortMode](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGridDataColumn.SortMode) property to `Custom`.
5. Handle the Grid's [CustomSort](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid.CustomSort) event and compare rows by their selection state in the event handler.

You can now sort data against the service column to move selected rows to the top.

## Files to Review

* [Index.razor](./CS/SortFilterBySelection/Components/Pages/Index.razor)
* [Index.razor.css](./CS/SortFilterBySelection/Components/Pages/Index.razor.css)

## Documentation

- [Selection and Focus in Blazor Grid](https://docs.devexpress.com/Blazor/404461/components/grid/selection)
- [Sort Data in Blazor Grid](https://docs.devexpress.com/Blazor/404460/components/grid/data-shaping/sort-data)
- [Filter Data in Blazor Grid](https://docs.devexpress.com/Blazor/404326/components/grid/data-shaping/filter-data/filter-data)

## More Examples

- [Blazor Grid - Custom Sorting](https://github.com/DevExpress-Examples/blazor-dxgrid-custom-sorting)
- [Blazor Grid - Delete Selected Rows](https://github.com/DevExpress-Examples/blazor-dxgrid-delete-selected-rows)

<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=blazor-dxgrid-sort-filter-by-selection&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=blazor-dxgrid-sort-filter-by-selection&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
