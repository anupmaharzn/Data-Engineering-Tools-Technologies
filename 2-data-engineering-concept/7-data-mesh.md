# Data Mesh

- `Data Mesh` is a new approach to `data management` that seeks to provide a `different` kind of approach to handling `all of an organization's data`, regardless of `where it resides`.

- It was introduced by `Zhamak Dehghani` in a `2020 article` titled **"How to Move Beyond a Monolithic Data Lake to a Distributed Data Mesh."**

- The traditional approach to handling data in organizations often involves creating a centralized `data lake` or `warehouse` where all data is `stored and managed. `

- However, as organizations grow, this `centralized model` can face `challenges` in terms of `scalability`, `agility`, and `ownership`.

- `Data Mesh` proposes a `decentralized` approach to data architecture treating `data as a product` and applying principles similar to those of `microservices architechture`.

- **Key Principle**
    - `Data ownership`
        - Data Mesh suggests distributing data ownership to individual domains within an organization.
        - Each domain is responsible for its data, making it easier to manage and understand. **(Data ownership by domain)**

    - `Data as a product`
        - Treat `data as a product` with clear `ownership`, `accountability`, and a `focus` on providing data services to other parts of the organization. 
    
    - `Self-serve Data infrastructure as a platform`
        - Provide infrastructure tools and platforms that enable domain teams to `build`, `deploy` and `manage` their own data products.**(Data available everywhere,self serve)**

    - `Federated governance`
        - Federated governance in a data mesh describes a situation in which `data governance` standards are defined `centrally`,but `local domain teams` have the `autonomy` and `resources` to execute these standards however is most appropriate for their particular environment.**(Data governed wherever it is)**


![datamesh](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/e31385f7-d894-4c03-9a06-88029da5ce3f)


