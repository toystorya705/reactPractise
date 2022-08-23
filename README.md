# import React, { Component } from "react";
class Counter extends Component {
  state = {
    count:0,
    imageUrl: "https://picsum.photos/200",
    tags: ["tag1", "tag2", "tag3"]
  };
  render() {
    
    return (

       
      <React.Fragment>
        {/* <img scr={this.state.imageUrl}/>
        <span className={this.getBadgeClasses()}> {this.formatCount()}</span>
        <button className="btn btn-secondary btn-sm">Increment </button> */}
      <ul>
       {this.renderTags()}
      </ul>
      </React.Fragment>
    );
  }

  renderTags(){
    if(this.state.tags.length===0) return <p>There are no tgs left</p>;

    return  this.state.tags.map(tag => <li key={tag}>{tag}</li>);
    
  
}

//     getBadgeClasses() {
//         let classes = "badge m-2 badge-";
//         classes += (this.state.count) == 0 ? "warning" : "primary";
//         return classes;
//     }

//   formatCount(){
//     const {count}=this.state;
//     return count === 0 ? "ZERO" : count;
//   }
}

export default Counter;
