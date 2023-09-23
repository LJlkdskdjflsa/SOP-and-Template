// update remote
git submodule update --init --recursive --remote

// add tag
./xdev/dev-tools/tag-tool/tag.sh

./xdev/dev-tools/tag-tool/tag.sh {service-name}
// ./xdev/dev-tools/tag-tool/tag.sh web-api


//
git tag -a v0.0.0.1-230607

token in core (sandbox):
`eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoiZm9hZFc4MzY5REtNUExTYys3WEJtYnJpY01UcGowQVdpYXJyODdoZy9CST0iLCJyb2xlcyI6IkFMTCIsImlhdCI6MTY5NDYwMjc1OCwiZXhwIjoxODUwMTIyNzU4fQ.JsAm0jtMjGhLHvVPvLEpsc3_ekQwLn0Hn-4POhSH6FA`
`eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoiQjZXNjlaTVZJd3dObGNDaHZkcTJpS0pZUEkzdmxVMnBhOUFlTjFMNnBscz0iLCJyb2xlcyI6IkFMTCIsImlhdCI6MTY5NDYwMjc5MiwiZXhwIjoxODUwMTIyNzkyfQ.wW9Ogx5o1Cp7XzpX-i-B31dUoNXY3YmrsChu3tNtDDM`
`eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoiTGRYeEJzUExpZHVxN1Jzb0pYelhOc1J0cEFyUWREL0hpMjR4dnZJQUZGMD0iLCJyb2xlcyI6IkFMTCIsImlhdCI6MTY5NDYwMjgwMiwiZXhwIjoxODUwMTIyODAyfQ.i2LVr8Vb7WY-VLOqZsKDF17aVb4sz2RbpukigfDq8iA`
`eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoiV1IyK1RiNEh0ZDVEcTVJRytXeDhPUld5QVdiZWZzYmR3aUduQThzdkhOST0iLCJyb2xlcyI6IkFMTCIsImlhdCI6MTY5NDYwMjgwOSwiZXhwIjoxODUwMTIyODA5fQ.ByXgsAe-YBGSVjVM_4wsGRLda436Q5EI55b5Xhp9u4s`
`eyJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoiRytVU1pxN0YrcnBYYi9BeEhTQkE4Y1A4ejY3Sm03Z0lrL1JML2RSREtGRT0iLCJyb2xlcyI6IkFMTCIsImlhdCI6MTY5NDYwMjgxOSwiZXhwIjoxODUwMTIyODE5fQ.q1DhY43JzPka4m_CbTpwSmGypl0XLkRRy6FVG99tjw0`

how to generate token:
```bash
curl --location 'https://partner-api.core.xrex.works/internal/v1/partner/tokens' \
--header 'exchange-token: 1eb87f7f4ee6e479' \
--header 'Content-Type: application/json' \
--data '{
    "user_id":27741
}'
```