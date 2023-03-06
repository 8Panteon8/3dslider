# 3D slider

**Video background implementation**:
```html
<video src="videos/smoke-background-optimized.mp4" class="showcase__video" autoplay loop muted></video>
```
**Lamp animation**
```css
@keyframes k-light {
  0% {
    opacity: 0.2;
  }
  50% {
    opacity: 0.3;
  }
  100% {
    opacity: 0.2;
  }
}
```

**Animation items**

- Splitting objects in half

```css
.showcase-carousel__image-left {
  perspective-origin: left center;
  clip-path: polygon(0 0, 50% 0, 50% 100%, 0 100%);
}
.showcase-carousel__image-right {
  perspective-origin: right center;
  clip-path: polygon(50% 0, 100% 0, 100% 100%, 50% 100%);
}
```

- Half animation

```css
@keyframes k-left-side {
  0% {
    transform: rotateY(-1deg) scaleX(0.92);
  }
  100% {
    transform: rotateY(0deg) scaleX(1);
  }
}
@keyframes k-right-side {
  0% {
    transform: rotateY(0deg) scaleX(1);
  }
  100% {
    transform: rotateY(1deg) scaleX(0.92);
  }
}

.showcase-carousel__image-left .showcase-carousel__image {
  animation: k-left-side 2s ease-in-out infinite;
  animation-direction: alternate;
}
.showcase-carousel__image-right .showcase-carousel__image {
  animation: k-right-side 2s ease-in-out infinite;
  animation-direction: alternate;
}

```






# Features
- Сustom design 
- Individual fonts
- Video Backgroung 
- 3D animations



# References
- [Bootstrap-breakpoint](https://getbootstrap.com/docs/4.6/getting-started/introduction/)


## Screenshot

![ezgif com-video-to-gif-4](https://user-images.githubusercontent.com/113831614/223225218-ac1f68c5-7644-4619-a58c-0b5c4d212a63.gif)
