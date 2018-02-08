# Dynamic Nav Link Creator

Will create nav link elements by passing params to the funciton.

```
export const FreakingAwesomeNavLink = ( {label, to, generalClassName, activeOnlyWhenExact } ) => {
    return (
      <Route path={to} exact={activeOnlyWhenExact} children={ ({match}) => {
        return (
        <li className={`${generalClassName}${match ? ' active' : ''}`}>
          <Link to={to} style={ {fontWeight: 'normal'} }>{label}</Link>
        </li>
        )}
      } />
    );
};
```
