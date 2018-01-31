# Snippets for Sorting, Filtering, Mapping

## Auto Suggest for Search

this snippet includes filtering an array from state (users in this case) and sorting on the input value (also held in state)
then the return from that is put into filteredUsers which is then used by the .map in the return to display all the results. 
Note the use of .toLowerCase() to remove case sensitivity.

```
render() {
    let filteredUsers = this.state.users.filter( (user) => {
        return user.name.toLowerCase().indexOf(this.state.input) !== -1;
      }
    )
    console.log(filteredUsers)

    return (
      <div>
          <input id="searchBox" placeholder="Search..." onChange={this.handleChange}/>
          <div id="listofUsers">
            {filteredUsers.map(users => <ul key={users.id} value={users.name} onClick={this.handleSelect}>{users.name} </ul>)}
          </div>
      </div>
    );
  }
```
