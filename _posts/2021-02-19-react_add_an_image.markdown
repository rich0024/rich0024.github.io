---
layout: post
title:      "React Add an Image"
date:       2021-02-19 18:09:42 +0000
permalink:  react_add_an_image
---


How do we add in an image or a pdf to a react project?

This is a simple task that was easier than expected. As I am building a portfolio site, one element to add will be images of myself. So, here are the simple steps I took to add an image.

First, find an image and add the file to the "assets" folder of your react project.

Next, add he import of the image to the component:
```
import cropped from '../assets/cropped.png'
```

Lastly, source the image with an 'img' tag.
```
export class bio extends Component {
    render() {
        return (
            <div>
                <img src={cropped}></img>
            </div>
        )
    }
}

export default bio
```
