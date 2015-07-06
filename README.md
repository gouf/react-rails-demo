# React + Rails

## Gem

* react-rails [reactjs/react-rails - Github](https://github.com/reactjs/react-rails)

## Setup

```bash
echo 'gem "react-rails"' >> Gemfile
bundle

rails g react:install
```

### Edited files

app/assets/javascripts/application.js

```javascript
//= require react
//= require react_ujs
//= require components
```

app/assets/javascripts/components/mycomponent.js.jsx.coffee

```coffeescript
@MyComponent = React.createClass
  render: ->
    `<div>
      Hello {this.props.name}
    </div>`
```

app/views/users/index.html.slim

```slim
= react_component 'MyComponent', name: 'Gouf'
```
