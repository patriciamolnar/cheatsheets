# Cypress Cheatsheet

## Commands
- `cy.visit('/')`: Orders browser to visit given URL. Cypress appends the path to the `baseUrl`. If no `baseUrl` set, specify full qualified URL.
- `cy.title()`: Returns page title

### Assertions

**Useful Links**
[Chai Assertions Library](https://www.chaijs.com/api/bdd/) | 
[Cypress Docs Assertions](https://docs.cypress.io/guides/references/assertions)


**[equal](https://www.chaijs.com/api/bdd/#method_equal)**
- `cy.title().should('equal', 'Page title')`: `equal` uses the `===` comparison

**include**
- `cy.title().should('include', 'Angular')`

**not**
- `.should('not.equal', 'Yan')`
- `expect(name).to.not.equal('Yan')`

**deep**
- `should('deep.equal', { name: 'Yan' })`
- `expect(obj).to.deep.equal({ name: 'Yan' })`

**nested**
- `.should('have.nested.property', 'a.b[1]')`
- `.should('nested.include', {'a.b[1]': 'y'})`
- `expect({ a: { b: 'x' }}).to.have.nested.property('a.b')`
- `expect({ a: { b: 'x' }}).to.nested.include({ 'a.b': 'x' })`

**ordered**
- `should('have.ordered.members', [1, 2])`
- `expect([1, 2]).to.have.ordered.members([1, 2])`
- `expect([1, 2]).not.to.have.ordered.members([2, 1])`



## Angular Specific
`ng e2e` Run Angular e2e tests
