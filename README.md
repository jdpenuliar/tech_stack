# tech_stack
const reducerHaha = (state = [], action) => {
  if(action.type === 'haha'){
    return action.payload.split('');
  }else if(action.type == 'haha2'){
    return [ ..state, action.payload];
  }
  return state;
};

const store = Redux.createStore(reducerHaha);

store.getState();

const action = {type: 'haha', payload: 'asdf'};
const action2 = {type: 'haha2', payload: 'haha'};

store.dispatch(action);
store.getState();

store.dispatch(action2);
store.getState();
