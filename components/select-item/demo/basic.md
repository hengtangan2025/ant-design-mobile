# 基本

- order: 0

列表主体内容的容器。

---

````jsx
import { List, SelectItem, Button, WingBlank, WhiteSpace } from 'antm';
import { createForm } from 'rc-form';

let SelectItemExample = React.createClass({
  onClick() {
    console.log(this.props.form.getFieldsValue());
  },
  render() {
    const {getFieldProps} = this.props.form;
    return (<div>
      <List>
        <List.Body>
          <SelectItem
            {...getFieldProps('select1', {
              initialValue: '2',
              valuePropName: 'value'
            })}
            label="下拉框"
            name="select1"
            align="right"
            options={[{val:'1', txt:'文本内容1'}, {val:'2', txt:'文本内容2'}, {val:'3', txt:'文本内容3'}]}
          />
          <SelectItem
            {...getFieldProps('select2', {
              initialValue: '3',
              valuePropName: 'value'
            })}
            name="select2"
            options={[{val:'1', txt:'文本内容1'}, {val:'2', txt:'文本内容2'}, {val:'3', txt:'文本内容3'}]}
          />
        </List.Body>
      </List>
      <WhiteSpace/>
      <WingBlank>
        <Button onClick={this.onClick}>确认添加</Button>
      </WingBlank>
    </div>);
  }
});

SelectItemExample = createForm()(SelectItemExample);

ReactDOM.render(<SelectItemExample/>, document.getElementById('components-select-item-demo-basic'));
````