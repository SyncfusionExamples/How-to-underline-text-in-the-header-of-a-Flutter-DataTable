# How to underline text in the header of a Flutter DataTable (SfDataGrid)?

In this article, we will show you how to underline text in the header of a [Flutter DataTable](https://www.syncfusion.com/flutter-widgets/flutter-datagrid).

Initialize the [SfDataGrid](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/SfDataGrid-class.html) widget with all the necessary properties. The [GridColumn.label](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/GridColumn/label.html) property is used to display the desired widget in a column header. Within the label property of [GridColumn](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/GridColumn-class.html), the corresponding header text widget is loaded. To underline the text, set [TextDecoration.underline](https://api.flutter.dev/flutter/dart-ui/TextDecoration/underline-constant.html) in the style property of Text. Additionally, you can adjust the underline thickness using [decorationThickness](https://api.flutter.dev/flutter/painting/TextStyle/decorationThickness.html).

```dart
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Syncfusion Flutter DataGrid')),
      body: SfDataGrid(
        source: employeeDataSource,
        columnWidthMode: ColumnWidthMode.fill,
        columns: <GridColumn>[
          GridColumn(
            columnName: 'id',
            label: Container(
              padding: EdgeInsets.all(16.0),
              alignment: Alignment.center,
              child: Text(
                'ID',
                style: TextStyle(
                  decoration: TextDecoration.underline,
                  decorationThickness: 3.0,
                ),
              ),
            ),
          ),
          GridColumn(
            columnName: 'name',
            label: Container(
              padding: EdgeInsets.all(8.0),
              alignment: Alignment.center,
              child: Text(
                'Name',
                style: TextStyle(
                  decoration: TextDecoration.underline,
                  decorationThickness: 2.0,
                ),
              ),
            ),
          ),
          GridColumn(
            columnName: 'designation',
            label: Container(
              padding: EdgeInsets.all(8.0),
              alignment: Alignment.center,
              child: Text(
                'Designation',
                style: TextStyle(
                  decoration: TextDecoration.underline,
                  decorationThickness: 2.0,
                ),
                overflow: TextOverflow.ellipsis,
              ),
            ),
          ),
          GridColumn(
            columnName: 'salary',
            label: Container(
              padding: EdgeInsets.all(8.0),
              alignment: Alignment.center,
              child: Text(
                'Salary',
                style: TextStyle(
                  decoration: TextDecoration.underline,
                  decorationThickness: 2.0,
                ),
              ),
            ),
          ),
        ],
      ),
    );
  }
```

You can download this example on [GitHub](https://github.com/SyncfusionExamples/How-to-underline-text-in-the-header-of-a-Flutter-DataTable).