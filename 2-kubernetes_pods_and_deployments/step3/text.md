
* create a simple nginx pod called `test` using commandline (imperative)

<details>
  <summary>Solution</summary>
    <pre><code>    
        kubectl run test --image=nginx
    </code></pre>
</details>

* create a simple nginx pod called `test2` in a declarative

<details>
  <summary>Solution</summary>
    <pre>
        <code>
        apiVersion: v1
        kind: Pod
        metadata:
            name: test2
        spec:
            containers:
            - name: nginx
              image: nginx
        </code>
        <code>
        kubectl create -f jack.yaml
        </code>
    </pre>
</details>
