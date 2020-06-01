```@meta
CurrentModule = StructuralCausalModels
```

## scm_path
```@docs
scm_path(parts...)
```

## DAG
```@docs
DAG
DAG(name::AbstractString, d::OrderedDict{Symbol, Vector{Symbol}}, df::DataFrame)
```

## d_separation
```@docs
d_separation(d::DAG, first::Vector{Symbol}, second::Vector{Symbol}, cond::SymbolList=nothing)
```

## shipley_test
```@docs
shipley_test(d::DAG)
```

## basis_set
```@docs
basis_set(dag::DAG)
```

## ancestral_graph
```@docs
ancestral_graph(d::DAG, m::Vector{Symbol}, c::Vector{Symbol})
ancestral_graph(a::NamedArray{Int, 2}, m::Vector{Symbol}, c::Vector{Symbol})
```


### Internals
```@docs
dag_vars(d::OrderedDict{Symbol, Vector{Symbol}})
edge_matrix(d::OrderedDict{Symbol, Vector{Symbol}})
edge_matrix(a::NamedArray, inv=false)
adjacency_matrix(d::OrderedDict{Symbol, Vector{Symbol}})
adjacency_matrix(e::NamedArray)
topological_order(a::NamedArray)
topological_sort(a::NamedArray)
ancester_graph(e::NamedArray)
indicator_matrix(e::NamedArray)
transitive_closure(a::NamedArray)
induced_covariance_graph(d::DAG, sel::Vector{Symbol}, cond::SymbolList; debug=false)
pcor(u::Vector{Symbol}, S::NamedArray)
```