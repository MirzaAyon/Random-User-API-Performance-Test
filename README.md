## Performance testing of [random-data-api](https://random-data-api.com/api/v2/users)

demo website : [random-data-api](https://random-data-api.com/api/v2/users)
- https://random-data-api.com/api/v2/users

### Steps of creating JMeter test
- Start JMeter
- Test plan creation
- Thread group
- Sampler(http)
- Listener
- Run

### Steps of creating thread properties for expected TPS
- 1,20000 users will use this website within 12 hours
- So total users 1,20000 and total time - 12*60*60 = 43,200 second
- now number of threads(users) - 1,20000 / 43,200 = 2.77 per second
- in 60 seconds it will be 166 users
- in 300 seconds it will be 833 users
- in 600 seconds it will be 1666 users
- in 900 seconds it will be 2499 users
- so I fixed it as 2499 users in 900 seconds
- with 1 loop count
- so finally our number of users - 2499
- numbers of second is - 900
- number of loop count - 1
- Highest actual TPS - 2.8
- All tests passed

### Steps of creating thread properties for bottleneck/stress test point
- time 900 seconds
- User 2,500 to 20,000 gradually
- Highest TPS - 22.2
- All tests passed
- Capacity -9,800 users
- Highest error rate 0.01%
- Bottleneck point(1% error) - No found

### Expected TPS Google drive link and screenshot

- Drive link: https://docs.google.com/spreadsheets/d/1rnamaVvXVe06k0wSKub2qqPPssgMP5SDyBSOwHhWf4A/edit?usp=sharing




### Bottleneck/Stress test point Google drive link and screenshot

- Drive link: https://docs.google.com/spreadsheets/d/1tkrLRpf4UcDk5tnIxyG85nf3Erkn4L1JrKVhKSQ4lN4/edit?usp=sharing


