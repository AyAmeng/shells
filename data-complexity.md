#O^2

## Description 

```typescript

.ts /** File */

```

## Code Source

```typescript

export interface Rule<T, S> {
  move: (data: T) => boolean
  left: S | string
  right: S | string
}

export class Machine<T, S> {
  private rules: Map<string, Rule<T, S>> = new Map()

  constructor(private initial: string) {}

  rule(
    name: string,
    move: (data: T) => boolean,
    left: S | string,
    right: S | string
  ) {
    this.rules.set(name, { move, left, right })
    return this
  }

  transition(data: T): S {
    let rule = this.rules.get(this.initial)

    while (true) {
      if (!rule) {
        throw Error(`Cannot found rule: ${this.initial}`)
      }

      const ret = rule.move(data)

      if (!!ret) {
        const r = this.rules.get(rule.left as string)
        if (r) {
          rule = r
          continue
        }
        return rule.left as S
      } else {
        const r = this.rules.get(rule.right as string)
        if (r) {
          rule = r
          continue
        }
        return rule.right as S
      }
    }
  }
}

```

## Usage

```typescript

export enum EndPoint {
  normal = 0,
  spec = 1,
  other = 2,
  borther = 3,
  sister = 4
}

const machine = new Machine<T extends SpecType, EndPoint>('root')

machine
  .rule('first', (p) => p.A, EndPoint.normal, 'second')
  .rule('sencond', (p) => p.B, 'third', EndPoint.sister)
  .rule('third', (p) => p.C, EndPoint.borther, 'end')
  .rule('end', (p) => p.D, EndPoint.other, 'first')

export const CPipe = (P: SpecType) => machine.transition(plan)


const source = (P: SpecType) => CPipe(P) /** WANT RESULT */

```

