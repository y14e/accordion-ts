# accordion.ts

WAI-ARIA compliant [accordion](https://www.w3.org/WAI/ARIA/apg/patterns/accordion/) pattern implementation in TypeScript.

## Usage

```ts
import Accordion from './accordion';

new Accordion(root, options);
// => Accordion
//
// root: HTMLElement
// options (optional): AccordionOptions

```

### 🪄 Options

```ts
interface AccordionOptions {
  animation?: {
    duration?: number; // ms (default: 300)
    easing?: string;   // <easing-function> (default: 'ease')
  };
  selector?: {
    content?: string;  // (default: ':has(> [data-accordion-trigger]) + *')
    trigger?: string;  // (default: '[data-accordion-trigger]')
  };
}
```

### 📦 API

#### open

```ts
accordion.open(trigger);
// => void
//
// trigger: HTMLElement
```

#### close

```ts
accordion.close(trigger);
// => void
//
// trigger: HTMLElement
```

#### destroy

Destroys the instance and cleans up all event listeners.

```ts
accordion.destroy(isForce);
// => Promise<void>
//
// isForce (optional): If true, skips waiting for animations to finish.
```

## Demo

https://y14e.github.io/accordion-ts/
