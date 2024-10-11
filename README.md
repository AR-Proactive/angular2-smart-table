# Angular Smart Table Component


## 🚀 This fork will be updated and maintained! 🚀

I'm a self-employed developer so any help is welcome, open a pull request and help me improve this library



## NEW Features

* 🚀 Added hide/show row  
* 🚀 Added Expandable Row (thanks [Samir](https://github.com/mominsamir))
* 🚀 Added Column resizing (thanks [dreswgfuse](https://github.com/dreswgfuse))
* 🚀 Added Multi Select for a column (thanks [thangluu93](https://github.com/thangluu93))
* 🚀 Added type to Settings object
* 🚀 Added Column resizing (thanks [dreswgfuse](https://github.com/dreswgfuse))
* 🚀 Added custom action render component (thanks [bacali95](https://github.com/bacali95))
* 🚀 Added Column sorting/filtering to nested objects (thanks [TejinderEvry](https://github.com/TejinderEvry))
* 🚀 Added row data to custom component render (thanks [marchrius](https://github.com/marchrius))
* 🚀 Include row data when invoking filterFunction (thanks [darrenhollick](https://github.com/darrenhollick))
* 🚀 Ability to select a row programmatically (thanks [NicolaLC](https://github.com/NicolaLC))

## Features

* Local data source (Server/API DataSource is on its way)
* Filtering
* Sorting
* Pagination
* Inline Add/Edit/Delete
* Flexible event model

## Installation

The library is available as npm package, so all you need to do is to run the following command:

```
npm i angular2-smart-table
```

This command will create a record in your `package.json` file and install the package into the npm modules folder.



## Minimal Setup Example

First thing you need to do is to import the angular2-smart-table directives into your component.

```

import { Angular2SmartTableModule } from 'angular2-smart-table';

```

Then register it by adding to the list of directives of your module:

```
// ...

@NgModule({
  imports: [
    // ...
    
    Angular2SmartTableModule,
    
    // ...
  ],
  declarations: [ ... ]
})
// ...
```

Now, we need to configure the table and add it into the template. The only <strong>required</strong> setting for the component to start working is a columns configuration.
Let's register <i>settings</i> property inside of the component where we want to have the table and configure some columns [Settings documentation](https://github.com/dj-fiorex/angular2-smart-table):
    
```
settings: Settings = {
  columns: {
    id: {
      title: 'ID'
    },
    name: {
      title: 'Full Name'
    },
    username: {
      title: 'User Name'
    },
    email: {
      title: 'Email'
    }
  }
};
```

Finally let's put the angular2-smart-table component inside of the template:

```
// ...

@Component({
  template: `
    <angular2-smart-table [settings]="settings"></angular2-smart-table>
  `
})
// ...
```
At this step you will have a minimal configured table. All functions are available by default and you don't need to configure them anyhow, so now you can add/edit/delete rows, sort or filter the table, etc.
 
Still it seems like something is missing... Right, there is no data in the table by default. To add some, let's create an array property with a list of objects in the component. Please note that object keys are the same as in the columns configuration.

```
data = [
  {
    id: 1,
    name: "Leanne Graham",
    username: "Bret",
    email: "Sincere@april.biz"
  },
  {
    id: 2,
    name: "Ervin Howell",
    username: "Antonette",
    email: "Shanna@melissa.tv"
  },
  
  // ... list of items
  
  {
    id: 11,
    name: "Nicholas DuBuque",
    username: "Nicholas.Stanton",
    email: "Rey.Padberg@rosamond.biz"
  }
];
```

And pass the data to the table:

```
// ...

@Component({
  template: `
    <angular2-smart-table [settings]="settings" [source]="data"></angular2-smart-table>
  `
})
// ...
```

Now you have some data in the table. -->
 
## Further Documentation
Installation, customization and other useful articles: https://github.com/dj-fiorex/angular2-smart-table

## How can I support developers?
- Star our GitHub repo :star:
- Create pull requests, submit bugs, suggest new features or documentation updates :wrench:


## License
[MIT](LICENSE.txt) license.
