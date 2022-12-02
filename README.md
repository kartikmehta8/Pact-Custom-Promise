<p align="center">
  <img src="https://user-images.githubusercontent.com/77505989/205330352-a0053d85-74bb-457f-ab4b-e46dda06d2b1.png" alt="BANNER" />
</p>

# Promise
A JavaScript Promise object contains both the producing code and calls to the consuming code:

```javascript
let myPromise = new Promise(function(myResolve, myReject) {
// "Producing Code" (May take some time)

  myResolve(); // when successful
  myReject();  // when error
});

// "Consuming Code" (Must wait for a fulfilled Promise)
myPromise.then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
```

When the producing code obtains the result, it should call one of the two callbacks:

| **Result**	 | **Call**                 |
| -------------|--------------------------|
| Success    	 | myResolve(result value)  |
| Error	       | myReject(error object)   |

# Promise Object Properties
A JavaScript Promise object can be:
- Pending
- Fulfilled
- Rejected

The Promise object supports two properties: **state** and **result**.

While a Promise object is "pending" (working), the result is undefined.

When a Promise object is "fulfilled", the result is a value.

When a Promise object is "rejected", the result is an error object.

| **myPromise.state** |	**myPromise.result** |
|---------------------|----------------------|
| "pending"           |          	undefined  |
| "fulfilled"         |     	a result value |
| "rejected"	        |      an error object |

### Pact is a custom implementation of JavaScript's Promise.
