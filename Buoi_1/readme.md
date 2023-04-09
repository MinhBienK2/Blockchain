# 1. Blockchain là gì?

+ Blockchain là một công nghệ đang trở nên phổ biến và được sử dụng rộng rãi trong nhiều lĩnh vực khác nhau. Nó là một hệ thống phân tán, được xây dựng trên nền tảng mã hóa và sử dụng các thuật toán đặc biệt để đảm bảo tính toàn vẹn, an toàn và tin cậy cho các giao dịch.

+ Theo đó, blockchain là một cơ chế lưu trữ thông tin được phân tán trên nhiều nút (node) máy tính khác nhau, mỗi nút đều giữ một bản sao của dữ liệu. Dữ liệu này được sắp xếp theo các block liên kết với nhau, tạo thành một chuỗi khối (blockchain) không thể sửa đổi hay thay đổi.

+ Blockchain cho phép các giao dịch được thực hiện một cách an toàn và bảo mật, bởi vì các giao dịch này được mã hóa và xác thực bởi các nút trong mạng. Khi một giao dịch được thêm vào blockchain, nó sẽ trở thành một phần của chuỗi khối và không thể bị xóa hoặc sửa đổi. Điều này đảm bảo tính toàn vẹn và tin cậy cho các giao dịch trên mạng.

+ Blockchain được sử dụng rộng rãi trong các ứng dụng tiền điện tử (cryptocurrency) như Bitcoin và Ethereum, tuy nhiên nó cũng có thể được áp dụng trong nhiều lĩnh vực khác như bảo hiểm, y tế, giáo dục, quản lý chuỗi cung ứng, bầu cử điện tử, và nhiều ứng dụng khác.

## Một số cơ chế hoạt động

+ Hashing: Hashing là một quá trình biến đổi dữ liệu đầu vào thành một chuỗi số hoặc ký tự có độ dài cố định.Trên một block trong blockchain, có 2 ô mã hash chính là mã hash của block trước đó và mã hash của các giao dịch trong block hiện tại. Mã hash của block trước đó được sử dụng để xác nhận tính toàn vẹn của blockchain, đồng thời giúp định vị vị trí của block hiện tại trong chuỗi blockchain. Mã hash của các giao dịch trong block hiện tại cũng được tính toán và lưu trữ trên block để đảm bảo tính toàn vẹn của dữ liệu. Khi một block mới được thêm vào blockchain, mã hash của nó sẽ được tính toán lại và xác thực bằng mã hash của block trước đó để đảm bảo tính toàn vẹn của chuỗi blockchain.

+ Peer-to-Peer (P2P): Mạng lưới blockchain được xây dựng trên cơ chế peer-to-peer (P2P), cho phép các node kết nối và trao đổi dữ liệu với nhau mà không cần thông qua trung tâm trung gian. Mỗi node trong mạng lưới blockchain được coi như là một ngang hàng với các node khác và có trách nhiệm xác minh và xử lý các giao dịch mới được thêm vào mạng lưới. Cơ chế P2P cũng giúp tăng tính bảo mật và khó khăn cho kẻ tấn công tấn công vào mạng lưới.

+ Consensus mechanism: Trong một mạng lưới blockchain, các node cần đồng ý về trạng thái của sổ cái, bao gồm các giao dịch đã diễn ra. Cơ chế đồng thuận là một thành phần quan trọng của mạng lưới blockchain cho phép các node đồng ý về tính hợp lệ của các giao dịch và trạng thái của sổ cái.Thông thường, nếu số phiếu ủng hộ đạt trên 50%, quyết định được xem như đã được đưa ra. Các cơ chế đồng thuận phổ biến nhất trong các mạng lưới blockchain bao gồm Proof of Work (PoW), Proof of Stake (PoS), Delegated Proof of Stake (DPoS) và Practical Byzantine Fault Tolerance (PBFT).

# 2. Các tính chất của Blockchain?

> ## Decentralization

+ Tính chất đầu tiên của blockchain là Decentralization, tức sự phi tập trung. Trong blockchain, không có một bên nào độc quyền kiểm soát hoặc quản lý toàn bộ hệ thống. Thay vào đó, hệ thống được phân tán trên nhiều máy tính, mỗi máy tính được gọi là một node, và tất cả các node này đều có thể truy cập và cập nhật dữ liệu.

+ Việc phân tán này giúp tăng tính bảo mật và độ tin cậy của hệ thống, vì không có một điểm duy nhất mà kẻ tấn công có thể tấn công và phá vỡ toàn bộ hệ thống. Thay vào đó, các node đóng vai trò như các quản trị viên độc lập, mỗi node chỉ kiểm soát một phần nhỏ của hệ thống, nhưng đồng thời đảm bảo tính phi tập trung của hệ thống.

+ Ngoài ra, tính chất phi tập trung này cũng giúp đảm bảo tính công bằng và minh bạch trong hệ thống blockchain. Tất cả các node đều có thể xem và xác nhận các giao dịch, và không ai có thể can thiệp vào hệ thống một cách ngầm định hay thay đổi dữ liệu một cách trái phép mà không được sự đồng ý của phần lớn các node khác trong hệ thống.

> ## Distributed

+ Tính chất thứ hai của blockchain là Distributed, tức sự phân tán. Trong blockchain, dữ liệu và các giao dịch được phân tán trên nhiều node khác nhau, chứ không chỉ lưu trữ trên một máy tính duy nhất. Mỗi node sẽ giữ một bản sao của toàn bộ blockchain và sẽ được đồng bộ hóa với các node khác.

+ Việc phân tán này giúp tăng tính bảo mật và độ tin cậy của hệ thống, vì nếu một node bị tấn công hay hỏng hóc, các node khác vẫn có thể hoạt động tiếp tục và đảm bảo tính toàn vẹn của hệ thống. Ngoài ra, việc phân tán này cũng giúp tăng tốc độ xử lý và giảm độ trễ, vì các node có thể xử lý các giao dịch đồng thời và song song với nhau.

+ Tuy nhiên, tính chất phân tán này cũng đặt ra một số thách thức về đồng bộ hóa dữ liệu giữa các node và việc đảm bảo tính nhất quán của hệ thống. Do đó, trong blockchain, các thuật toán phân tán và đồng bộ hóa được sử dụng để đảm bảo tính phân tán và đồng nhất của dữ liệu trên toàn bộ hệ thống.

> ## Immutability

+ Tính chất thứ ba của blockchain là Immutability, tức tính không thể thay đổi. Điều này có nghĩa là một khi một khối dữ liệu (block) đã được thêm vào blockchain, nó sẽ không thể bị sửa đổi hay xóa bỏ.

+ Cơ chế bảo đảm tính không thể thay đổi này được xây dựng trên cơ sở mã hóa băm (hashing) và mối quan hệ giữa các khối dữ liệu trong blockchain. Khi một khối mới được thêm vào blockchain, nó sẽ được liên kết với khối trước đó thông qua mã băm của khối trước đó. Mã băm này cũng được lưu trữ trong khối hiện tại, giúp người dùng kiểm tra tính toàn vẹn của blockchain và đảm bảo rằng không có khối nào bị thay đổi.

+ Việc đảm bảo tính không thể thay đổi của blockchain rất quan trọng trong các ứng dụng như tiền điện tử hay lưu trữ dữ liệu quan trọng. Nó giúp người dùng tin tưởng vào tính toàn vẹn của dữ liệu và đảm bảo rằng không ai có thể can thiệp hoặc thay đổi dữ liệu trong hệ thống.

> ## Transparency

+ Tính chất thứ tư của blockchain là Transparency, tức tính minh bạch. Điều này có nghĩa là mọi giao dịch được thực hiện trên blockchain đều được công khai và có thể được xem trực tiếp bởi bất kỳ ai trong mạng.

+ Mỗi giao dịch trên blockchain được lưu trữ trong một khối dữ liệu (block) và mỗi khối này được liên kết với các khối trước đó, tạo thành một chuỗi liên kết (blockchain). Khi một khối mới được thêm vào blockchain, toàn bộ mạng sẽ nhận được thông tin về khối đó, bao gồm cả các giao dịch được thực hiện trong khối đó. Bất kỳ ai trong mạng đều có thể kiểm tra và xem thông tin về các giao dịch này.

+ Điều này giúp đảm bảo tính minh bạch và công khai của hệ thống. Không có một đơn vị nào có quyền kiểm soát hoặc che giấu thông tin, mà mọi người đều có thể theo dõi và kiểm tra tính toàn vẹn của hệ thống. Tính minh bạch này cũng giúp đẩy mạnh sự tin tưởng của người dùng vào blockchain, đặc biệt là trong các ứng dụng liên quan đến tài chính hay lưu trữ dữ liệu quan trọng.

> ## Security

+ Tính chất thứ năm của blockchain là Security, tức tính an toàn và bảo mật. Hệ thống blockchain được thiết kế với mục đích đảm bảo an toàn cho các giao dịch và dữ liệu trên mạng.

+ Một trong những cách mà blockchain đảm bảo tính an toàn là thông qua cơ chế Proof-of-Work (PoW) hoặc Proof-of-Stake (PoS). Khi thực hiện một giao dịch, người dùng phải giải mã một thuật toán phức tạp để chứng minh rằng họ đã thực hiện giao dịch đó. Quá trình này yêu cầu năng lượng và thời gian, và chỉ những người có khả năng tính toán cao mới có thể thực hiện được. Điều này ngăn chặn các hacker hoặc tấn công mạng từ việc tấn công và thay đổi các giao dịch trên blockchain.

+ Ngoài ra, các khối dữ liệu trên blockchain được mã hóa bằng các thuật toán bảo mật mạnh, ngăn chặn các tấn công từ bên ngoài. Điều này đảm bảo rằng các giao dịch và dữ liệu trên blockchain được bảo mật và không thể bị thay đổi hay xâm nhập một cách dễ dàng.

+ Tính chất bảo mật của blockchain là một trong những yếu tố quan trọng giúp đảm bảo tính tin cậy và sự phổ biến của nó trong các lĩnh vực như tài chính, chứng khoán, bảo hiểm và lưu trữ dữ liệu quan trọng.

# 3. Node là gì?

+ Node trong blockchain là một phần của hệ thống, đóng vai trò là nút mạng hoặc nút tham gia vào quá trình xác minh và lưu trữ các giao dịch trên blockchain. Các node có thể được cài đặt trên bất kỳ thiết bị nào có kết nối Internet, từ máy tính để bàn, máy chủ, thiết bị di động, đến các thiết bị Internet of Things (IoT).

+ Mỗi node trong blockchain hoạt động như một nút mạng độc lập, hoạt động đồng thời với các nút khác để tạo ra một hệ thống phân tán và giúp xác minh và xử lý các giao dịch trên mạng. Mỗi node có quyền truy cập vào toàn bộ lịch sử giao dịch trên blockchain và cập nhật nó bằng cách lưu trữ các khối mới nhất trên mạng.

+ Các node trong một mạng blockchain có thể được phân thành các loại khác nhau, bao gồm full node, light node và masternode. Full node là loại node hoàn chỉnh, có thể kiểm tra tất cả các giao dịch trên mạng và lưu trữ toàn bộ blockchain. Light node là loại node nhẹ hơn, chỉ cần lưu trữ một phần của blockchain để xác minh các giao dịch. Masternode là loại node đặc biệt được sử dụng trong các mạng blockchain có chức năng thêm các tính năng đặc biệt như Dash hay PIVX.

+ Tóm lại, node trong blockchain là một thành phần quan trọng của mạng, đóng vai trò trong quá trình xác minh và lưu trữ các giao dịch trên blockchain. Việc có nhiều node trên mạng giúp tăng tính phân tán và đảm bảo tính bảo mật của hệ thống.

# 4. Block là gì?

+ Trong blockchain, block (khối) là một phần quan trọng của chuỗi khối, nơi chứa thông tin về các giao dịch mới nhất được thêm vào blockchain. Mỗi block chứa một danh sách các giao dịch mới nhất cùng với một header (tiêu đề) bao gồm các thông tin như định danh khối (block hash), phiên bản của phần mềm đang sử dụng, thời gian tạo khối và địa chỉ của block trước đó trên chuỗi khối.

+ Mỗi block trên chuỗi khối có một kích thước giới hạn, thường được xác định bởi giao thức blockchain mà nó thuộc về. Ví dụ, kích thước block trên Bitcoin là 1MB, trong khi đó Ethereum cho phép kích thước block tối đa là 15MB.

+ Các block trên chuỗi khối được liên kết với nhau theo thứ tự thời gian, trong đó mỗi block sẽ trỏ đến block trước đó trên chuỗi khối bằng cách sử dụng địa chỉ của block trước đó. Quá trình liên kết các block này lại với nhau tạo thành một chuỗi khối đầy đủ, được gọi là blockchain.

+ Việc sử dụng block để lưu trữ thông tin về các giao dịch trên mạng blockchain giúp tăng tính bảo mật và độ tin cậy của hệ thống, bởi vì mỗi block được xác thực và mã hóa một cách độc lập, và việc thay đổi bất kỳ thông tin nào trong block đó sẽ làm thay đổi định danh của block, gây ra sự không thống nhất trong chuỗi khối.

