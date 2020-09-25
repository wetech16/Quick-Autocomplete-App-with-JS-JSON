# Quick Autocomplete App with JS & JSON

## html

    - index.html
        - css { bootstrap.min.css }
        - icon { fontawesome }
        - input { id="search" }
        - div { id="match-list" }
        - script { js/main.js }

---

    - fontawesome: `<link>`

## JS

    - main.js
        -search { getElementById { search } } }
            - addEventListener { input, searchStates { search.value } }
                 - searchStates { async searchText }
                    - res { await fetch { DATA } }
                    - states { await res.json() }
                    - matches { states }
                        - filter { state }
                            - regex { RegExp{`^${ searchText }`, 'gi' } }
                            - return state
                                - name.match { regex }
                                - abbr.match { regex }
                    - if { searchText.length }
                        - matches
                        - matchList.innerHTML
                    - outputHtml { matches }
                        - html { matches }
                            - map
                                - h4 { match.,name, match.captical, etc }
                                - <small>Lat { match.lat, etc }

## CSS

    - bootstrap.min.css

---

- bootstrap.min.css: Download From Bootswatch. it's a free themes from bootstrap

## DATA

    - states.json
