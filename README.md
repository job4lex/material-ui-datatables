# Material-UI-Datatables

[![npm](https://img.shields.io/npm/v/material-ui-datatables.svg)](https://www.npmjs.com/package/material-ui-datatables)

An another React Data tables component.  
Material-UI-Datatables is a custom [React](https://facebook.github.io/react/) component using awesome [Material-UI](http://www.material-ui.com/). It provides filter and column sort and pagination features to display data mostly in desktop applications. You can check about the component in [Google's guideline](https://material.google.com/components/data-tables.html).

## Installation
```sh
npm install material-ui-datatables
```

## Demo
[Demo](https://hyojin.github.io/material-ui-datatables/)

## Status
Work in progress

## Usage
```jsx
import React, {Component} from 'react';
import DataTables from 'material-ui-datatables';

const TABLE_COLUMNS = [
  {
    key: 'name',
    label: 'Dessert (100g serving)',
  }, {
    key: 'calories',
    label: 'Calories',
  },
  ...
];

const TABLE_DATA = [
  {
    name: 'Frozen yogurt',
    calories: '159',
    fat: '6.0',
    carbs: '24',
    protein: '4.0',
    sodium: '87',
    calcium: '14%',
    iron: '1%',
  }, {
    name: 'Ice cream sandwich',
    calories: '159',
    fat: '6.0',
    carbs: '24',
    protein: '4.0',
    sodium: '87',
    calcium: '14%',
    iron: '1%',
  },
  ...
];

class MyComponent extends Component {
  ...
  render() {
    return (
      <DataTables
        height={'auto'}
        selectable={false}
        showRowHover={true}
        columns={TABLE_COLUMNS}
        data={TABLE_DATA}
        showCheckboxes={false}
        onCellClick={this.handleCellClick}
        onCellDoubleClick={this.handleCellDoubleClick}
        onFilterValueChange={this.handleFilterValueChange}
        onSortOrderChange={this.handleSortOrderChange}
        page={1}
        count={100}
      />
    );
  }
}
```

## License
MIT
