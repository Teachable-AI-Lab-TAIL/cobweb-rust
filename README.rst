=================
COBWEB with Rust
=================

This is a Rust library of algorithms that perform COBWEB.

In this library, the `COBWEB
<http://axon.cs.byu.edu/~martinez/classes/678/Papers/Fisher_Cobweb.pdf>`_ 
is implemented. 

Written by Anusha Srinivasa. Last updated: Oct 2022
use std::collections::HashMap;

struct CobwebNode{
    concept_id:u32,
    count:f32,
    av_counts:HashMap<String, HashMap<String, f32>>,
    children:Vec<*mut CobwebNode>,
    parent:*mut CobwebNode, 
    tree:*mut CobwebTree
}

static _counter: u32 = 0;
impl CobwebNode{
    fn new(other_node:*mut CobwebNode) -> CobwebNode {
        object = CobwebNode{
            count: 0.0,
            av_counts: HashMap::new(),
            children: Vec::new()
        }
        object.concept_id = object.gensym();
        
        return object;
    }
    fn gensym(&self)->u32{
        _counter += 1;
        return _counter;
    }
}

struct CobwebTree{
    root: *mut CobwebNode
}

impl CobwebTree{
    fn new(&self){
        
    }
}
fn main()
{

}
