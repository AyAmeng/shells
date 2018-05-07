
```ts
import * as React from 'react'
import hoistNonReactStatics from 'hoist-non-react-statics'

// inheritance Inversion & 渲染劫持
export const PaymentUiDecorator = (projectId?: string) => {
  console.info(projectId)
  return function (WrappedComponent: React.ComponentClass) {
    class HOCWrapper extends WrappedComponent {

      handleUpgrade = () => {
        console.info('upgrade app')
      }

      render () {

        const newProps = {
          handleUpgrade: this.handleUpgrade
        }
        return <WrappedComponent { ...this.props } { ...newProps } />
      }
    }

    return  hoistNonReactStatics(HOCWrapper, WrappedComponent)
  }
}

// props proxy
export const PaymentEventDecorator = (projectId?: string) => {
  console.info(projectId)
  return function (WrappedComponent: React.ComponentClass<any>) {
    class HOCWrap extends React.Component {

      handleUpgrade = () => {
        console.info('upgrade app')
      }

      render () {
        const newProps = {
          handleUpgrade: this.handleUpgrade
        }
        return <WrappedComponent { ...this.props } { ...newProps } />
      }
    }

    return hoistNonReactStatics(HOCWrap, WrappedComponent)
  }
}

type Props = {
  isValid: boolean
  onPassComponent: JSX.Element | null
  onPayComponent: JSX.Element | null
}

type PaymentWallProps = Readonly<Props>

export class PaymentWall extends React.PureComponent<PaymentWallProps, {}> {

  render() {
    console.info('payment wall')
    return this.props.isValid ? this.props.onPassComponent : this.props.onPayComponent
  }
}
```
