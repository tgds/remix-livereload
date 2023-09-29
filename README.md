# Remix LiveReload

Same as Remix's LiveReload, but it exposes a handle to listen to HMR updates. Useful if you need to do some work after HMR updates, like reloading i18n translations.

## Usage

Same as you would use Remix's LiveReload, but you can pass a callback using the `onHMR` prop. In your root file:

```js
import { LiveReload } from "remix-livereload";

export default function App() {
	const handleHMR = useCallback((hmrEvent) => {
		console.log(hmrEvent);
	}, []);

	return (
		<html>
			<head></head>
			<body>
				<LiveReload onHMR={handleHMR} />
			</body>
		</html>
	);
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
