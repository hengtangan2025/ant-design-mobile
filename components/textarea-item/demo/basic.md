# 基本

- order: 0

列表主体内容的容器。

---

````jsx
import { List, TextareaItem, Button, WingBlank, WhiteSpace } from 'antm';
import { createForm } from 'rc-form';

let TextareaItemExample = React.createClass({
  onClick() {
    console.log(this.props.form.getFieldsValue());
  },
  render() {
    const { getFieldProps } = this.props.form;
    return (
      <div>
        <List>
          <List.Body>
            <TextareaItem
              {...getFieldProps('note', {
                initialValue: 'dada22东方朔放松放松东方朔放松放松冯绍峰放松放松放松放松放松放松放松放松',
                valuePropName: 'value'
              })}
              label="备注说明"
              name="yyy"
              rows={5}
              placeholder="带清除"
              clear={true}
              onBlur={function(){console.log('onBlur'); }}
              onFocus={function(e){console.log('onFocus'); console.log(e);}}
            />
            <TextareaItem
              {...getFieldProps('note2', {
                initialValue: '',
                valuePropName: 'value'
              })}
              label="备注说明"
              name="yyy"
              placeholder="请填写"
              clear={false}
              rows={5}
              maxLength={100}
              onBlur={function(){console.log('onBlur');}}
              onFocus={function(e){console.log('onFocus'); console.log(e);}}
            />
            <TextareaItem
              {...getFieldProps('note3', {
                initialValue: '',
                valuePropName: 'value'
              })}
              label="备注说明"
              placeholder="请填写"
            />
            <TextareaItem
              {...getFieldProps('note4', {
                initialValue: '',
                valuePropName: 'value'
              })}
              label="备注说明"
              clear={true}
              placeholder="请填写"
            />
          </List.Body>
        </List>
        <WhiteSpace/>
        <WingBlank>
          <Button onClick={this.onClick}>确认添加</Button>
        </WingBlank>
      </div>
    );
  }
});

TextareaItemExample = createForm()(TextareaItemExample);

ReactDOM.render(<TextareaItemExample/>, document.getElementById('components-textarea-item-demo-basic'));
````