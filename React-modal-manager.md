# React Instance Manager

## Location

```sh

Typescript

```

## Code
```sh

import React from 'react'
import * as ReactDOM from 'react-dom'

class ModalManager {

  private mountNode: HTMLElement | undefined
  private instance: React.ReactNode = null

  private static createMountNode() {
    const el = document.createElement('span')
    document.body.appendChild(el)
    return el
  }

  open(node: React.ReactNode) {
    if (!this.mountNode) {
      this.mountNode = ModalManager.createMountNode()
    }

    if (node) {
      this.instance = node
      this.render()
    }
  }

  close() {
    if (this.mountNode) {
      this.instance = null
      this.render()
    }
  }

  private render() {
    ReactDOM.render(
      <div>{ this.instance }</div>
    , this.mountNode!)
  }

}

export const modalMgr = new ModalManager()

```
