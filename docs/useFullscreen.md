# `useFullscreen`

在iOS上为全屏视频显示一个元素全屏、可选回退。

## Usage

```jsx
import useFullscreen from 'react-use/lib/useFullscreen';
import useToggle from 'react-use/lib/useToggle';

const Demo = () => {
  const ref = useRef(null)
  const [show, toggle] = useToggle(false);
  const isFullscreen = useFullscreen(ref, show, {onClose: () => toggle(false)});

  return (
    <div ref={ref} style={{backgroundColor: 'white'}}>
      <div>{isFullscreen ? 'Fullscreen' : 'Not fullscreen'}</div>
      <button onClick={() => toggle()}>Toggle</button>
      <video src="http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4" autoPlay />
    </div>
  );
};
```

## Reference

```ts
useFullscreen(ref, show, {onClose})
```
