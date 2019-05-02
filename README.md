# react-draftjs-render
#### Universal React DraftJS render component

This component can render DraftJS data into React DOM, React Native or any other React renderer.

```
npm install react-draftjs-render
```

Example usage:
```javascript
import Render from 'react-draftjs-render'

// .....

const RenderDraftJSRichText = () => (
  <Render 
    data={dataObjectTakenFromDraftJS}
    getBlockComponent={(blockType) => null}
    getStyleComponent={(style) => null}
    getEntityComponent={(entityType) => null}
    textComponent={SomeTextComponent}
    />
)

```

Although you will want to fill these props with appropriate functions most of the time, you only need `data` prop for very basic rendering for React DOM.

`getBlockComponent` takes block type and returns component or an array [component, wrapperComponent] (mostly used for nested lists).

`getStyleComponent` takes style text and returns component.

`getEntityComponent` takes entity type and returns component.

`textComponent`, you need to set this to ReactNative `Text` component for rendering text in React Native.
