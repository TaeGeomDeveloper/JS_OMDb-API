# JS_OMDb-API
OMDb API 학습

## The Open Movie Database

[OMDb API](http://www.omdbapi.com/)

[Axios](https://axios-http.com/kr/docs/intro)

- Query String
  주소? 속성 = 값&속성 = 값&속성 = 값
  
  ```javascript
    import axios from 'axios'

    function fetchMovies() {
      axios.get('https://www.omdbapi.com/?apikey=341fc161&s=frozen')
      .then((res) => {
        console.log(res)
        const h1El = document.querySelector('h1');
        const imgEl = document.querySelector('img')
        h1El.textContent = res.data.Search[0].Title
        imgEl.src = res.data.Search[0].Poster
      })
    }
    fetchMovies()
  ```

