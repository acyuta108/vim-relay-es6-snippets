vim-relay-es6-snippets
==================

A set of snippets for Vim to work with Facebook's [Relay](http://facebook.github.io/relay/) library.

Requires [vim-snipmate](https://github.com/garbas/vim-snipmate).

Use along [vim-react-es6-snippets](https://github.com/bentayloruk/vim-react-es6-snippets). Thanks Ben!

Installation
============

Use your preferred Vim plugin installation method.  Vundle or Pathogen should be fine (I use Pathogen).

Usage
=====

Within any Javascript or JSX file, you should be able to do the following:

(in insert mode)
```
rcc<Tab>
```

expanding to

```
export default Relay.createContainer(Component, {
  fragments: {
    propName: () => Relay.QL`
      fragment on _ComponentConnection {
        count,
        edges {
          node {
            id,
            text,
            ${ChildComponent.getFragment('child')}
          }
        }
      }
    `
  },
});
```

Current list of snippets
------------------------

__relcc__ Relay.createContainer

__relmut__ Relay.Mutation

__relgf__ getFragment

__relfrag__ fragment

__relfragconn__ fragment on connection

__relsu__ Relay.Store.update
