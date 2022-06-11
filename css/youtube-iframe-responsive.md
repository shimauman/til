## Version
- 

## Samples
If use Gatsby and Tailwind CSS...

Sample1
```
  <div className="w-full" style={{ aspectRatio: "16 / 9" }}>
    <iframe
      className="w-full h-full"
      width={***}
      height={***}
      ***
    />
  </div>
```

or

Sample2
```
  // 56.25% is same with aspectRatio: "16 / 9".
  <div className="relative h-0 overflow-hidden" style={{ paddingBottom: "56.25%" }}>
    <iframe
      className="absolute top-0 left-0 w-full h-full"
      width={***}
      height={***}
      ***
    />
  </div>
```

- Sample 1 depends on the browser supports `aspectRatio`.

## Reference
- [`aspect-ratio` browser compatibility](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/aspect-ratio#browser_compatibility)
