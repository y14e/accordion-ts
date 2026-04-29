# accordion.ts

WAI-ARIA compliant [accordion](https://www.w3.org/WAI/ARIA/apg/patterns/accordion/) pattern implementation in TypeScript.

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
    easing?: string; // <easing-function> (default: 'ease')
  };
  selector?: {
    content?: string;
    trigger?: string;
  };
}
```

## Demo

https://y14e.github.io/accordion-ts/
