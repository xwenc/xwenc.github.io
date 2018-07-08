---
title: sync submit for redux form and saga
layout: post
tags: react
---

I do not know if these action creators are new or have some downside, but could we not just use the startSubmit and stopSubmit action creators and pass the form name with the submit action?

Example:
```
function* createEntity(entity, apiFn, formId, newEntity) {
  yield put( entity.request() )
  yield put( startSubmit(formId) )
  const {response, error} = yield call(apiFn, newEntity)
  if(response) {
    yield put( entity.success(response) )
    yield put( reset(formId) )
    yield put( stopSubmit(formId) )
  }
  else {
    yield put( entity.failure(error) )
    // handle and format errors from api
    yield put( stopSubmit(formId, serverValidationErrors) )
  }
}
```
Quite new to both redux-form and redux-saga, so there could be something i am missing here.