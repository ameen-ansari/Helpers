## Canvas setup in react app

`Install the following dependency`
```
npm i fabric
```
`Initialize the canvas element`

```
   <div className="w-full h-full flex justify-center items-center">
       <canvas width={"auto"} height="auto" id="canvas" />
   </div>
```

`Innitialize the fabric`

```
  useEffect(() => {
    const canvas = new fabric.Canvas("canvas", {
      height: 500,
      width: 500,
      selection: false,
    });
// store the canvas ref in local store
    dispatch(updateCanvasRef(canvas));
  }, []);
```

Save the canvas ref in your local redux store



