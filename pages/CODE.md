- ```closure
      {:title "🔥 OVERDUE"
      :query [:find (pull ?h [*])
              :in $ ?start ?next
              :where
              [?h :block/marker ?marker]
              (or [?h :block/scheduled ?d]
              [?h :block/deadline ?d])
              [(contains? #{"TODO" "DOING" "NOW" "LATER" "WAITING"} ?marker)]
              [(>= ?d ?start)]
              [(<= ?d ?next)]]
      :inputs [:365d :1d]
      :result-transform (fn [result]
                          (sort-by (fn [h]
                                     (get h :block/priority "Z")) result))
      :collapsed? false
      :breadcrumb-show? false}
  ```
-
-